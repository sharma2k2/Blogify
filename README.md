📖 Blogify

Blogify is a Blog Application built using Node.js, Express, MongoDB, and EJS as part of my MCA 3rd Semester Training Project at Geetanjali Institute of Technical Studies.
It demonstrates user authentication, blog post creation, editing, and management with a simple and responsive UI.

✨ Features

🔑 User Authentication – Register, Login, Logout with secure password hashing (bcryptjs).
📝 Create & Manage Blogs – Add, edit, delete, and view personal blog posts.
📂 Upload Feature – Supports image uploads using Multer.
👤 Profile & Settings – Update username, password, bio, and view all your posts.
📅 Post Tracking – Displays creation and last update timestamps.
🎨 EJS Templates – Dynamic rendering for clean, reusable UI.
💾 Session Management – Uses express-session & connect-mongo for secure sessions.

🛠 Technologies Used

Backend: Node.js, Express.js
Frontend: EJS templating engine
Database: MongoDB (local instance)
Authentication: express-session, bcryptjs
File Upload: multer
Development Tools: nodemon

⚙️ Installation & Setup

Initialize project (if needed)
npm init -y

Install dependencies
npm install express ejs mongoose express-session body-parser connect-mongo bcryptjs multer
npm install nodemon --save-dev

▶️ Running the Application
Start the server in development mode:
npx nodemon app.js
Or run directly:
node app.js
#OR
npm start

Open in browser: http://localhost:8080

📂 Folder Structure
blog-upgrade/
│
├── config/
│   └── db.js               # MongoDB connection setup
│
├── controllers/
│   ├── authController.js   # Handles user signup/login
│   └── postController.js   # Handles create/edit/view/delete posts
│
├── middleware/
│   ├── authMiddleware.js   # Protect routes for authenticated users
│   └── uploadMiddleware.js # Handles file uploads
│
├── models/
│   ├── Post.js             # Post schema
│   └── User.js             # User schema
│
├── public/
│   ├── css/
│   │   └── style.css
│   ├── images/
│   │   └── blogify.png
│   └── uploads/            # Uploaded images
│
├── routes/
│   ├── auth.js             # Auth routes
│   └── post.js             # Post routes
│
├── views/
│   ├── allPosts.ejs
│   ├── editPost.ejs
│   ├── login.ejs
│   ├── myPosts.ejs
│   ├── newPost.ejs
│   ├── register.ejs
│   ├── viewPost.ejs
│   └── welcome.ejs
│
├── app.js                   # Main Express server
├── package-lock.json
├── package.json
└── txt.txt

💾 Database Setup

Install MongoDB locally and start the MongoDB server.
Database name: blogsdb
MongoDB connection (config/db.js):

const mongoose = require('mongoose');

const connectDB = async () => {
  try {
    await mongoose.connect('mongodb://127.0.0.1:27017/blogsdb', {
      useNewUrlParser: true,
      useUnifiedTopology: true
    });
    console.log("MongoDB Connected Successfully");
  } catch (err) {
    console.error("MongoDB Connection Failed", err);
    process.exit(1);
  }
};

module.exports = connectDB;


Collections:
users → Stores user data
posts → Stores blog posts with timestamps

📦 Dependencies

express – Web framework for Node.js
ejs – Templating engine for dynamic HTML
mongoose – MongoDB ORM
express-session – Session management
body-parser – Parses request bodies
connect-mongo – Store sessions in MongoDB
bcryptjs – Secure password hashing
multer – File upload handling
nodemon – Auto-restart server in development

🚀 Future Enhancements

🌐 Social login (Google, Facebook)
💬 Comments and likes for posts
📝 Rich text editor for blogs
🎭 Profile customization
📱 Improved mobile responsiveness

📚 Project Information

Project Name: Blogify
Semester: MCA 3rd Sem (2025)
Institute: Geetanjali Institute of Technical Studies
Developer: Kavita Sharma
Project Goal: Learn full-stack development with Node.js, Express, EJS, and MongoDB through a real-world blog application
