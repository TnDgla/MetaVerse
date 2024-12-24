---
# Project Name: Metaverse Application
Metaverse Application is a 2D multiplayer environment built using the MERN stack, WebSockets, and microservices. This project enables users to interact in virtual spaces, manage avatars, and collaborate in shared environments, focusing on scalable and efficient real-time communication.

---

### **Mission and Objectives**

---

#### **Mission:**
To develop a scalable, interactive metaverse application that facilitates real-time communication and virtual interactions among users in a 2D space.

---

#### **Objectives:**

1. **Real-Time Communication:**
   - Implement WebSockets for seamless bidirectional communication.
   - Ensure low-latency interaction for all users in shared spaces.

2. **User Management:**
   - Provide secure user authentication.
   - Allow customizable avatars for personalized experiences.

3. **Virtual Spaces:**
   - Enable users to create, manage, and interact in shared virtual environments.

4. **Scalability:**
   - Design architecture to handle multiple users and rooms efficiently.

5. **Deployment:**
   - Deploy the application to production-ready Kubernetes clusters.

---

### **Technology Stack**

#### **Frontend**
1. **React.js**
   - **Why?**: Simplifies building dynamic user interfaces.
   - **Use Case**: Handles user interaction and rendering of virtual spaces.

2. **Phaser.js**
   - **Why?**: Lightweight framework for 2D game development.
   - **Use Case**: Renders 2D environments and avatars.

#### **Backend**
1. **Node.js**
   - **Why?**: Enables efficient server-side development.
   - **Use Case**: Manages APIs and WebSocket connections.

2. **Express.js**
   - **Why?**: Simplifies API creation and routing.
   - **Use Case**: Defines REST APIs for user and space management.

3. **Socket.IO**
   - **Why?**: Facilitates real-time, bidirectional communication.
   - **Use Case**: Handles real-time user movements and interactions.

#### **Database**
1. **MongoDB**
   - **Why?**: Flexible schema design for managing spaces and user data.
   - **Use Case**: Stores user profiles, space metadata, and event logs.

#### **Deployment**
1. **Kubernetes**
   - **Why?**: Provides scalability and container orchestration.
   - **Use Case**: Hosts the backend and WebSocket services.

2. **Docker**
   - **Why?**: Simplifies containerization and deployment.
   - **Use Case**: Packages and deploys the application.

3. **Frontend Hosting:** Netlify or Vercel
   - **Why?**: Optimized platforms for React app hosting.
   - **Use Case**: Deploys the client-side application.

---

## **Workflow Overview**

The application workflow involves users entering virtual spaces, interacting with other users, and customizing their environments. Admins manage space configurations and user permissions. WebSockets ensure real-time updates and seamless user interactions.

### **FlowChart**

![image](https://github.com/user-attachments/assets/006506fd-b6f0-46ca-9988-35120a9e3109)

---

### **Project Structure for Feature Implementation**

This project is structured to ensure a systematic and incremental development process. Each week builds upon the previous deliverables, enabling a smooth transition from basic to advanced functionalities.

**NOTE:** Participants are encouraged to customize the design and functionality to make the application unique.

---

## **Week-by-Week Learning Plan**

---

### **Week 1: Project Setup and UI Design**
- **Goal:** Set up the foundational structure and design the application’s UI.
- **Tasks:**
  1. Initialize a **React.js** project with Phaser.js.
     - **Reading:** [React.js Official Docs](https://reactjs.org/docs/getting-started.html)
     - **Video:** [React.js Crash Course](https://www.youtube.com/watch?v=w7ejDZ8SWv8)
  2. Design basic layouts for user dashboard and space navigation.
     - **Reading:** [Phaser.js Documentation](https://phaser.io/)
     - **Video:** [Phaser.js Setup Guide](https://www.youtube.com/watch?v=0qtg-9M3peI)

- **Deliverables:**
  - Basic UI with placeholders for virtual spaces and avatar customization.

---

### **Week 2: User Authentication and Space Management**
- **Goal:** Implement user authentication and initial space management.
- **Tasks:**
  1. Set up user schemas in MongoDB.
     - **Reading:** [MongoDB Schema Design](https://mongoosejs.com/docs/guide.html)
     - **Video:** [Mongoose Models Tutorial](https://www.youtube.com/watch?v=DZBGEVgL2eE&t=30s)
  2. Build authentication APIs with JWT.
     - **Reading:** [JWT Basics](https://jwt.io/introduction/)
     - **Video:** [JWT Authentication Guide](https://www.youtube.com/watch?v=mbsmsi7l3r4)
  3. Create endpoints for space creation and retrieval.
     - **Reading:** [RESTful API Design](https://restfulapi.net/)
     - **Video:** [Building REST APIs](https://www.youtube.com/watch?v=pKd0Rpw7O48)

- **Deliverables:**
  - Functional authentication and basic space management APIs.

---

### **Week 3: Real-Time Features**
- **Goal:** Develop real-time interaction using WebSockets.
- **Tasks:**
  1. Implement a WebSocket server using Socket.IO.
     - **Reading:** [Socket.IO Docs](https://socket.io/docs/v4/)
     - **Video:** [Real-Time Apps with Socket.IO](https://www.youtube.com/watch?v=O6JcOfhHz8k)
  2. Enable real-time user movements and space interactions.
     - **Reading:** [Phaser.js Game Loop](https://phaser.io/tutorials/making-your-first-phaser-3-game/part3)
     - **Video:** [Phaser.js Real-Time Guide](https://www.youtube.com/watch?v=K1nPd4ZibVc)

- **Deliverables:**
  - Real-time interaction between users in virtual spaces.

---

### **Week 4: Avatar Customization and Advanced Space Features**
- **Goal:** Allow users to customize avatars and enhance space functionality.
- **Tasks:**
  1. Build APIs for avatar customization and element placement.
     - **Reading:** [MongoDB Advanced Schemas](https://www.mongodb.com/docs/manual/)
     - **Video:** [API Development Best Practices](https://www.youtube.com/watch?v=7YcW25PHnAA)
  2. Implement dynamic space updates with WebSocket broadcasting.
     - **Reading:** [WebSocket Broadcasting](https://socket.io/docs/v4/broadcasting-events/)
     - **Video:** [Building Multiplayer Features](https://www.youtube.com/watch?v=5O-4QrO77cU)

- **Deliverables:**
  - Customizable avatars and dynamic space interactions.

---

### **Week 5: Deployment and Testing**
- **Goal:** Deploy the application and ensure optimal performance.
- **Tasks:**
  1. Deploy the application to Kubernetes.
     - **Reading:** [Kubernetes Basics](https://kubernetes.io/docs/tutorials/kubernetes-basics/)
     - **Video:** [Kubernetes Deployment Guide](https://www.youtube.com/watch?v=X48VuDVv0do)
  2. Test all functionalities and optimize for scalability.
     - **Reading:** [Testing Web Applications](https://www.postman.com/api-testing/)
     - **Video:** [Postman Testing Guide](https://www.youtube.com/watch?v=VywxIQ2ZXw4)

- **Deliverables:**
  - Fully deployed and functional Metaverse Application.

---
### Screenshots
![Screenshot (427)](https://github.com/user-attachments/assets/4b683783-889d-4b30-a407-aba351a65687)

---

### **References**
1. [React Documentation](https://reactjs.org/docs/getting-started.html)
2. [Phaser.js Documentation](https://phaser.io/)
3. [MongoDB Documentation](https://www.mongodb.com/docs/manual/)
4. [Socket.IO Documentation](https://socket.io/docs/v4/)
5. [Kubernetes Basics](https://kubernetes.io/docs/tutorials/kubernetes-basics/)
6. https://www.youtube.com/watch?v=aamk2isgLRk
7. https://github.com/hkirat/2d-metaverse/

