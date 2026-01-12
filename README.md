# 🔗 URL Shortener API

A **backend-only URL Shortener project** built using **Node.js, Express.js, and MongoDB**.  
This project provides REST APIs to generate short URLs and redirect them to original URLs.  
All APIs are tested using **Postman** (no frontend included).

---

## 🚀 Features

- Generate a unique short URL for any valid long URL
- Redirect short URL to the original URL
- Store URLs in MongoDB
- Track visit history / clicks
- RESTful API design
- Error handling and validation

---

## 🛠 Tech Stack

- **Node.js**
- **Express.js**
- **MongoDB**
- **Mongoose**
- **NanoID**
- **Postman** (for API testing)

---

## 📂 Project Structure

.
├── controllers/
│ └── url.js
├── models/
│ └── url.js
├── routes/
│ └── url.js
├── index.js
├── package.json
└── README.md

yaml
Copy code

---

## 📌 API Endpoints

### 1️⃣ Create Short URL
**POST** `/url`

**Request Body:**
```json
{
  "url": "https://example.com"
}
Response:

json
Copy code
{
  "shortID": "abc123xy"
}
2️⃣ Redirect to Original URL
GET /:shortId

Example:

bash
Copy code
http://localhost:8000/abc123xy
➡️ Redirects to original URL stored in database.

⚙️ Installation & Setup
1️⃣ Clone the repository

bash
Copy code
git clone https://github.com/your-username/url-shortener.git
2️⃣ Install dependencies

bash
Copy code
npm install
3️⃣ Start MongoDB locally

4️⃣ Run the server

bash
Copy code
npm start
Server will run on:

arduino
Copy code
http://localhost:8000
🧪 API Testing
All APIs are tested using Postman.

POST request for generating short URL

GET request for redirection

📌 Notes
This is a backend-focused project

No frontend included

Frontend can easily consume these APIs

Suitable for learning REST APIs and backend development
