# 🔗 URL Shortener with Authentication & Analytics

A full-stack URL Shortener application built using **Node.js, Express, MongoDB, and EJS**.  
The project includes **JWT-based authentication**, **role-based authorization**, **URL analytics**, and a **3D animated, glassmorphic UI** using pure CSS.

---

## ✨ Features

- 🔐 User authentication using **JWT & Cookies**
- 👥 Role-based access control (**ADMIN / NORMAL users**)
- 🔗 Generate short URLs using **nanoid**
- 📊 Track click analytics for each short URL
- 🛡 Protected routes using custom middleware
- 🧾 Separate dashboards for users and admin
- 🎨 3D animated, glassmorphic UI with realistic shadows
- 🧠 Clean MVC architecture

---

## 🛠 Tech Stack

### Backend
- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT (jsonwebtoken)

### Frontend
- EJS (Server-side rendering)
- HTML5
- CSS3 (3D animations, glassmorphism)

### Tools & Libraries
- nanoid
- cookie-parser
- nodemon

---

## 🔐 Authentication Flow

1. User signs up or logs in
2. On login, a **JWT token** is generated
3. Token is stored in **HTTP cookies**
4. On every request, middleware:
   - Reads token from cookies
   - Verifies JWT
   - Attaches user data to `req.user`
5. Access to routes is controlled using user roles

---

## 🔑 Authorization (Role Based)

- **NORMAL users**
  - Create short URLs
  - View only their own URLs

- **ADMIN users**
  - View all URLs created by all users
  - Access admin-only routes

---

## 🔗 URL Shortening Flow

1. User submits a long URL
2. Server generates a unique short ID using `nanoid`
3. URL is stored in MongoDB with:
   - original URL
   - short ID
   - visit history
   - creator ID
4. Visiting the short URL:
   - Redirects to original URL
   - Stores timestamp for analytics

---

## 📊 Analytics

Each short URL tracks:
- Total number of clicks
- Timestamp of every visit

Analytics are stored in MongoDB and can be accessed via protected routes.

---

## 🎨 UI & Styling

- Built using **pure CSS**
- Glassmorphic design
- 3D floating card animations
- Realistic shadows & depth
- Google Fonts (Poppins)

No external UI libraries used.
