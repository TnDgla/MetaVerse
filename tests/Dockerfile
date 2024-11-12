# Build stage
FROM node:18-alpine AS builder

# Set working directory
WORKDIR /app

# Add build essentials and git for potential dependencies
RUN apk add --no-cache python3 make g++ git

# Copy package files
COPY package*.json ./

# Add check for required files
RUN [ -f "package.json" ] || (echo "package.json is missing" && exit 1) && \
    [ -d "src" ] || (echo "src directory is missing" && exit 1)

# Install dependencies with specific npm config for better reliability
RUN npm config set network-timeout 600000 && \
    npm ci --quiet

# Copy source with specific excludes
COPY . .
COPY .env.production .env

# Verify and build
RUN npm run lint || exit 1 && \
    npm run test || exit 1 && \
    npm run build

# Add check for build output
RUN [ -d "dist" ] || (echo "Build failed - no dist directory" && exit 1)

# Production stage
FROM node:18-alpine

# Set environment variables
ENV NODE_ENV=production
ENV PORT=3000

# Install additional runtime dependencies
RUN apk update && \
    apk upgrade && \
    apk add --no-cache dumb-init curl bash && \
    adduser -D nodejs && \
    chown -R nodejs:nodejs /app

# Create app directory and set permissions
WORKDIR /app
RUN chown -R node:node /app

# Copy with explicit dist folder structure
COPY --from=builder --chown=nodejs:nodejs /app/dist ./dist
COPY --from=builder --chown=nodejs:nodejs /app/package*.json ./
COPY --from=builder --chown=nodejs:nodejs /app/.env ./

# Install production dependencies with specific config
RUN npm config set network-timeout 600000 && \
    npm ci --only=production --quiet && \
    npm cache clean --force

# Security scanning
RUN npm audit

# More robust healthcheck
HEALTHCHECK --interval=30s --timeout=5s --start-period=5s --retries=3 \
    CMD curl -f http://localhost:$PORT/health -H "Accept: application/json" || exit 1

# Use non-root user
USER nodejs

# Expose port
EXPOSE $PORT

# Use dumb-init as entrypoint
ENTRYPOINT ["/usr/bin/dumb-init", "--"]

# Start application
CMD ["npm", "start"]