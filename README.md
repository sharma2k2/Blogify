# 📖 Blogify – MERN Training Project

A Blog Application built using **Node.js, Express, MongoDB, and EJS** as part of my **MCA 3rd Semester Training Project** at **Geetanjali Institute of Technical Studies**.  
This project demonstrates **user authentication, blog post creation, editing, and management** with a simple, responsive UI.

---

## 📑 Table of Contents
- [✨ Features](#-features)
- [🛠 Technologies Used](#-technologies-used)
- [⚙️ Installation & Setup](#️-installation--setup)
- [▶️ Running the Application](#️-running-the-application)
- [📸 Screenshots](#-screenshots-optional)
- [📂 Folder Structure](#-folder-structure)
- [💾 Database Setup](#-database-setup)
- [📦 Dependencies](#-dependencies)
- [🚀 Future Enhancements](#-future-enhancements)
- [📚 Project Information](#-project-information)

---

## ✨ Features
- 🔑 **User Authentication** – Register, Login, Logout with secure password hashing (**bcryptjs**).  
- 📝 **Create & Manage Blogs** – Add, edit, delete, and view personal blog posts.  
- 📂 **Upload Feature** – Supports image uploads using **Multer**.  
- 👤 **Profile & Settings** – Update username, password, bio, and view your posts.  
- 📅 **Post Tracking** – Shows when a blog was created or last updated.  
- 🎨 **EJS Templates** – Dynamic rendering for clean and reusable UI.  
- 💾 **Session Management** – Uses `express-session` & `connect-mongo` for secure sessions.  

---

## 🛠 Technologies Used
- **Backend:** Node.js, Express.js  
- **Frontend:** EJS templating engine  
- **Database:** MongoDB (local instance)  
- **Authentication:** express-session, bcryptjs  
- **File Upload:** multer  
- **Development Tools:** nodemon  

---

## ⚙️ Installation & Setup  

1. **Initialize project**
   ```bash
   npm init -y
2. **Install dependencies**
   ```bash
   npm install express
   npm install ejs
   npm install mongoose
   npm install express-session
   npm install body-parser
   npm install connect-mongo
   npm install bcryptjs
   npm install multer
3. **Install dev dependency (for auto-reload during development)**
   ```bash
   npm install nodemon --save-dev
▶️ Running the Application

Start the app using nodemon:
```
npx nodemon app.js`
```
**Or run directly:**
```
node app.js
```
**or**
```
npm start
```

**Now open your browser and go to:**
👉 http://localhost:8080

---

📂 Folder Structure
```
blog-upgrade/
├── config/
│   └── db.js               # MongoDB connection setup
├── controllers/
│   ├── authController.js   # Handles user signup/login
│   └── postController.js   # Handles create/edit/view/delete posts
├── middleware/
│   ├── authMiddleware.js   # Protect routes for authenticated users
│   └── uploadMiddleware.js # Handles file uploads
├── models/
│   ├── Post.js             # Post schema
│   └── User.js             # User schema
├── public/
│   ├── css/
│   │   └── style.css
│   ├── images/
│   │   └── blogify.png
│   └── uploads/            # Uploaded images
├── routes/
│   ├── auth.js             # Auth routes
│   └── post.js             # Post routes
├── views/
│   ├── allPosts.ejs
│   ├── editPost.ejs
│   ├── login.ejs
│   ├── myPosts.ejs
│   ├── newPost.ejs
│   ├── register.ejs
│   ├── viewPost.ejs
│   └── welcome.ejs
├── app.js                   # Main Express server
├── package-lock.json
├── package.json
└── txt.txt`
```
---

## 💾 Database Setup

- Install MongoDB locally and start the MongoDB server.
- Database name: blogsdb
- Update MongoDB connection string in config/db.js:
```
const mongoose = require('mongoose');
mongoose.connect('mongodb://127.0.0.1:27017/blogsdb', {
    useNewUrlParser: true,
    useUnifiedTopology: true
})
.then(() => console.log("MongoDB connected successfully"))
.catch(err => console.error("MongoDB connection error:", err));
```
## Collections:
- users → Stores user data
- posts → Stores blog posts with creation/update timestamps

---

## 📦 Dependencies

- **express** – Web framework for Node.js
- **ejs** – Templating engine for dynamic HTML rendering
- **mongoose** – MongoDB ORM for database operations
- **express-session** – Session management
- **body-parser** – Parses incoming request bodies
- **connect-mongo** – Stores session in MongoDB
- **bcryptjs** – Hash passwords securely
- **multer** – Handles file uploads
- **nodemon** – Auto-restarts server during development

---

## 🚀 Future Enhancements

- 🌐 Social login (Google, Facebook)
- 💬 Comments and likes for posts
- 📝 Rich text editor for blogs
- 🎭 Profile customization for users
- 📱 Mobile responsive layout improvements

---

## 📚 Project Information

- **Project Name:** Blogify – MERN Stack Training Project
- **Semester:** MCA 3rd Sem (2025)
- **Institute:** Geetanjali Institute of Technical Studies
- **Developer:** Kavita Sharma
- **Project Goal:** Learn full-stack development with Node.js, Express, EJS, and MongoDB through a real-world blog application
