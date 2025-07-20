Got it. You want the preview section to clearly label the first image as the "Login Page" and the second as the "Chat Preview." That's a great way to guide visitors through the user experience.

Here is the updated README with the correctly labeled previews presented side-by-side.

# 🚀 Messenger App - Real-Time MERN Stack Chat App

A full-stack, real-time chat application built with MongoDB, Express, React, and Node.js. Features include live messaging, user authentication, and online status indicators.

[**➥ Live Demo Link**](https://quick-chat-client-mu.vercel.app/login)

### ✨ **App Preview**

<img src="https://github.com/user-attachments/assets/a0e6c522-13ab-48d2-b15f-5d85f98c85e8" alt="Login Page">
<img src="https://github.com/user-attachments/assets/8ed4c703-b393-45be-b94f-c37a0e315c5a" alt="Chat View">

### **Key Features**
*   **💬 Real-Time Messaging**: Instant chat powered by Socket.IO.
*   **🔐 User Authentication**: Secure sign-up and login functionality.
*   **🖼️ Cloud Media Storage**: Avatar uploads handled by Cloudinary.
*   **📱 Responsive Design**: A clean, modern UI for all devices.

### 💻 **Tech Stack**
*   **Frontend**: React, Vite
*   **Backend**: Node.js, Express.js
*   **Database**: MongoDB
*   **Real-Time**: Socket.IO

## 🛠️ **Local Setup Guide**

Get the project running on your machine in a few quick steps.

### **1. Get Your API Keys**
You'll need free API keys from:
*   [**MongoDB Atlas**](https://mongodb.com/cloud/atlas/register): Create a cluster and get your **Connection URI**. Remember to allow access from anywhere (0.0.0.0/0).
*   [**Cloudinary**](https://cloudinary.com/users/register_free): Get your **Cloud Name**, **API Key**, and **API Secret**.

### **2. Set Up the Backend**
1.  Navigate to the `/server` directory.
2.  Fill in the `/.env` file with the API keys you just obtained.
3.  In your terminal, run the following commands:
    ```bash
    # Install dependencies
    npm install

    # Start the server
    npm run server
    ```

### **3. Set Up the Frontend**
1.  Open a **new terminal** and navigate to the `/client` directory.
2.  Run the following commands:
    ```bash
    # Install dependencies
    npm install

    # Start the client
    npm run dev
    ```
Your application should now be running locally!

## ☁️ **Deployment to Vercel**

Deploy your app to the web for free.

1.  **Push to GitHub**: First, push your entire project to a GitHub repository.
2.  **Deploy the Server**:
    *   Create a **New Project** on Vercel and link your GitHub repository.
    *   Set the **Root Directory** to `server`.
    *   Add your environment variables from the `.env` file.
    *   Deploy and **copy the live server URL**.
3.  **Deploy the Client**:
    *   Create another **New Project** on Vercel using the same repository.
    *   Set the **Root Directory** to `client`.
    *   Add one environment variable: `VITE_BACKEND_URL` with the live server URL as its value.
    *   Deploy
