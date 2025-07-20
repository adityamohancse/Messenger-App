
🚀 Messenger - A Full-Stack Real-Time Chat Application

Welcome to Messenger! This is a complete real-time chat application built with the MERN stack (MongoDB, Express, React, Node.js). It features user authentication, online status indicators, and real-time messaging.

This guide will walk you through setting up the project locally and deploying it to the web using Vercel.

### **Features**
*   **Real-Time Messaging**: Instant message delivery using WebSockets.
*   **User Authentication**: Secure user sign-up and login.
*   **Online Status**: See which users are currently online.
*   **One-on-One Chats**: Private conversations between users.
*   **Cloud Media Storage**: User avatars and images are handled by Cloudinary.
*   **Responsive Design**: A clean and modern UI that works on all devices.

### **Tech Stack**
*   **Frontend**: React, Vite
*   **Backend**: Node.js, Express.js, Socket.IO
*   **Database**: MongoDB Atlas
*   **Media Storage**: Cloudinary
*   **Deployment**: Vercel

## **🛠️ Local Development Setup**

Follow these steps to get the project running on your local machine.

### **1. Prerequisites**
*   **Node.js**: Make sure you have Node.js installed. You can download it from [nodejs.org](https://nodejs.org/en/download/).
*   **Git**: You will need Git to clone and manage the project repository.

### **2. Environment Setup (API Keys)**
You need to get API keys from MongoDB and Cloudinary.

#### **MongoDB Atlas Setup**
1.  Go to [MongoDB Atlas](https://www.mongodb.com/cloud/atlas/register) and create a free account.
2.  Create a new **M0 (Free)** cluster.
3.  Create a **database user** with a username and a simple password (avoid special characters like `@` to prevent connection issues).
4.  Navigate to **Network Access**, click **Add IP Address**, and select **Allow Access from Anywhere** (0.0.0.0/0).
5.  Go back to **Database**, click **Connect** on your cluster, select **Drivers**, and copy the **MongoDB URI**.

#### **Cloudinary Setup**
1.  Create a free account on [Cloudinary](https://cloudinary.com/users/register_free).
2.  Navigate to your **Dashboard**.
3.  Find your **Cloud Name**, **API Key**, and **API Secret**. You will need all three.

### **3. Project Installation**
First, run the server, and then run the client.

#### **⚙️ Backend (Server) Setup**
1.  Open the project in your code editor (like VS Code).
2.  In the `server` folder, find the `.env` file. Fill in the placeholders with the keys you obtained earlier.
    ```env
    MONGO_URI=your_mongodb_uri_here
    CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
    CLOUDINARY_API_KEY=your_cloudinary_api_key
    CLOUDINARY_API_SECRET=your_cloudinary_api_secret
    ```
3.  Navigate into the `server` folder in your terminal:
    ```bash
    cd server
    ```
4.  Install the dependencies:
    ```bash
    npm install
    ```
5.  Start the server:
    ```bash
    npm run server
    ```
    The server should now be running on `http://localhost:5000`.

#### **🖥️ Frontend (Client) Setup**
1.  Open a **new terminal** window.
2.  Navigate into the `client` folder:
    ```bash
    cd client
    ```
3.  Install the dependencies:
    ```bash
    npm install
    ```
4.  Start the client application:
    ```bash
    npm run dev
    ```
    The chat application will now be running on its local URL (e.g., `http://localhost:5173`).

## **☁️ Deployment to Vercel**

Follow these steps to deploy your chat application to the web for free.

### **1. Push to GitHub**
Before deploying, you need to push your entire project to a GitHub repository.

### **2. Deploying the Backend (Server)**
1.  Go to [Vercel](https://vercel.com) and create a new project, linking it to your GitHub repository.
2.  In the project configuration, set the **Root Directory** to `server`.
3.  Expand the **Environment Variables** section. Copy and paste all the variables from your local `server/.env` file.
4.  Add one more environment variable:
    *   **Key**: `NODE_ENV`
    *   **Value**: `production`
5.  Click **Deploy**. Once finished, Vercel will provide you with a live URL for your server. Copy this URL.

### **3. Deploying the Frontend (Client)**
1.  Create another new project on Vercel, linking it to the **same** GitHub repository.
2.  This time, set the **Root Directory** to `client`.
3.  Expand the **Environment Variables** section and add one variable:
    *   **Key**: `VITE_BACKEND_URL` (or whatever the key is named in `client/.env`)
    *   **Value**: Paste the live server URL you copied from the previous step. **Make sure to remove any trailing slash (`/`) at the end.**
4.  Click **Deploy**.

Congratulations! Your full-stack chat application is now live on the internet.

[1] https://www.youtube.com/watch?v=9MGZT7LageI
