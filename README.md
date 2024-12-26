# MERN Social Media App

This project is a full-stack social media application built with the MERN stack (MongoDB, Express.js, React, Node.js). It includes features like user authentication, post creation, real-time updates, and more. The application is designed to provide a seamless user experience with modern web technologies and a responsive interface.

## Deployment
The application is deployed and accessible at: [https://social-media-ush6.onrender.com/](https://social-media-ush6.onrender.com/)

---

## Features

### 1. User Authentication
The application uses secure JWT (JSON Web Tokens) for authentication. Users can register, log in, and maintain their sessions securely. Passwords are hashed using bcrypt for added security.

### 2. Post Creation and Management
Users can create posts with text and images. They have the ability to edit or delete their posts. Posts are displayed in a feed that updates in real-time, allowing users to interact with the latest content.

### 3. Real-Time Updates
With Socket.IO, the app provides real-time updates for events like new posts or comments. This ensures a dynamic and engaging user experience.

### 4. Image Uploads
Images can be uploaded directly from the user’s device. The application uses Multer for handling file uploads and Cloudinary for hosting and managing images in the cloud.

### 5. Share Posts
Users can share posts with others, either within the platform or by copying a link to share externally. This feature enhances engagement and helps users spread content quickly.

### 6. Responsive Design
The frontend is built with TailwindCSS, a utility-first CSS framework, to ensure the app is fully responsive. It adapts seamlessly to different screen sizes, providing a consistent user experience across devices.

---

## Tech Stack

### Frontend:
- **React**: A JavaScript library for building user interfaces.
- **React Router DOM**: For managing navigation and routing within the application.
- **TailwindCSS**: For styling and responsive design.
- **Axios**: For making HTTP requests to the backend API.
- **React Icons**: For adding scalable vector icons.
- **React Hot Toast**: For displaying toast notifications.

### Backend:
- **Node.js**: A JavaScript runtime for building the server-side application.
- **Express.js**: A web application framework for Node.js.
- **MongoDB**: A NoSQL database for storing user and post data.
- **Mongoose**: An ODM (Object Data Modeling) library for MongoDB.
- **Socket.IO**: For real-time communication between the client and server.
- **Multer**: For handling file uploads.
- **Cloudinary**: For hosting and managing images in the cloud.

---

## Installation and Setup

### Prerequisites:
To run this project locally, ensure you have the following installed:
- Node.js
- MongoDB

### Steps:

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd mern-social
   ```

2. **Install backend dependencies:**
   ```bash
   npm install
   ```

3. **Navigate to the `frontend` directory and install frontend dependencies:**
   ```bash
   cd frontend
   npm install
   ```

4. **Set up environment variables:**
   Create a `.env` file in the root directory with the following variables:
   ```env
   PORT=5000
   MONGO_URI=<your-mongo-uri>
   JWT_SECRET=<your-jwt-secret>
   CLOUDINARY_CLOUD_NAME=<your-cloudinary-cloud-name>
   CLOUDINARY_API_KEY=<your-cloudinary-api-key>
   CLOUDINARY_API_SECRET=<your-cloudinary-api-secret>
   ```

5. **Start the development server:**
   - Backend:
     ```bash
     npm run dev
     ```
   - Frontend:
     ```bash
     cd frontend
     npm run dev
     ```

6. **Access the application:**
   Open your browser and navigate to `http://localhost:3000`.

---

## Detailed Scripts

### Backend:
- **`npm start`**: Starts the backend server.
- **`npm run dev`**: Starts the backend server with nodemon for live reloading. This is useful for development as it automatically restarts the server when changes are made.

### Frontend:
- **`npm run dev`**: Starts the frontend development server with Vite, providing fast and efficient hot module replacement.
- **`npm run build`**: Builds the frontend for production, optimizing assets and preparing the app for deployment.
- **`npm run preview`**: Previews the production build locally to test the optimized version.

---

## Deployment

### Preparation:
1. Ensure all dependencies are installed and the application builds correctly:
   ```bash
   npm run build
   ```

2. Verify that the environment variables are correctly set in the `.env` file.

### Deployment Steps:
1. Deploy the backend to a hosting platform like Render, Heroku, or AWS.
2. Deploy the frontend to a static hosting platform like Vercel, Netlify, or Render.
3. Update the environment variables on the hosting platform to match your `.env` file.

---

## Application Architecture

### Folder Structure:
- **Backend:** Contains the server-side code, API routes, and database models.
  - `backend/index.js`: Entry point for the backend server.
  - `backend/models`: Mongoose models for MongoDB.
  - `backend/routes`: API routes for handling requests.

- **Frontend:** Contains the client-side code and UI components.
  - `frontend/src`: React components and pages.
  - `frontend/src/styles`: TailwindCSS configurations and global styles.

### Data Flow:
1. **Frontend:**
   - User interacts with the UI.
   - React components make HTTP requests to the backend API via Axios.
2. **Backend:**
   - Express.js handles incoming requests.
   - Mongoose interacts with MongoDB to fetch or store data.
   - Socket.IO handles real-time communication.
3. **Database:**
   - MongoDB stores user data, posts, and other application data.

---

## Challenges Faced

### 1. Real-Time Functionality
Implementing real-time updates using Socket.IO required careful handling of events and ensuring synchronization between the client and server.

### 2. File Uploads
Managing file uploads securely and efficiently was a challenge. Using Multer and integrating with Cloudinary helped streamline this process.

### 3. Responsive Design
Ensuring a consistent and user-friendly interface across different devices required extensive testing and adjustments with TailwindCSS.

### 4. Deployment
Coordinating the deployment of both the frontend and backend while maintaining environment variable consistency posed some initial challenges.

---

## Future Enhancements

### Planned Features:
1. **Likes and Comments:**
   - Implement a feature to like posts and add comments.
2. **User Profiles:**
   - Add user profile pages with options to edit personal information and view user-specific posts.
3. **Notifications:**
   - Real-time notifications for events like new likes, comments, or messages.
4. **Search Functionality:**
   - Add a search bar to find users and posts easily.

### Scalability:
- Migrate to a cloud database like MongoDB Atlas for better scalability.
- Use a CDN for serving static assets to improve performance.

