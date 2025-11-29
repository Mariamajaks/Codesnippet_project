# Code Snippet API

## Overview
The Code Snippet API is a full-stack application that allows developers to save, retrieve, and organize reusable code snippets. Built with **Node.js**, **Express**, **MongoDB**, and optionally a simple frontend, this project demonstrates RESTful API design, database integration, and deployment.

---

## Features
- **Create snippets** with title, code, language, description, and tags
- **Retrieve all snippets** with optional filtering by language
- **Retrieve a single snippet** by ID
- **Store data** in MongoDB Atlas
- **Optional frontend** to display snippets

---

## Technologies Used
- Node.js
- Express.js
- MongoDB Atlas
- Mongoose (ORM for MongoDB)
- Postman (for testing API)
- HTML + JavaScript (optional frontend)

---

## Installation & Run Steps

### 1. Clone the repository

```bash
git clone https://github.com/Mariamajaks/Codesnippet_project.git
cd Codesnippet_project
2. Install dependencies
bash
Copy code
npm install
3. Setup environment variables
Copy .env.example to .env

Add your MongoDB URI:

ini
Copy code
MONGODB_URI=your_mongodb_connection_string
PORT=3000
4. Start the server
bash
Copy code
node server.js
Server will run on http://localhost:3000/

Test API endpoints with Postman

API Endpoints
Method	Endpoint	Description
GET	/	Test route, returns "Snippet API is running!"
GET	/api/snippets	Get all snippets
GET	/api/snippets?lang=javascript	Get snippets filtered by language
GET	/api/snippets/692ab93601be67694fcf5b33	Get one snippet by ID
POST	/api/snippets	Create a new snippet

Testing Instructions (Postman)
Create Snippet (POST)

URL: http://localhost:3000/api/snippets

Body (JSON):

json
Copy code
{
  "title": "Loop Example",
  "language": "javascript",
  "code": "for(let i=0; i<5; i++){ console.log(i); }",
  "description": "Basic loop example",
  "tags": ["loop", "js", "beginner"]
}
Get All Snippets (GET)

URL: http://localhost:3000/api/snippets

Filter Snippets by Language (GET)

URL: http://localhost:3000/api/snippets?lang=javascript

Get One Snippet (GET)

URL: http://localhost:3000/api/snippets/692ab93601be67694fcf5b33

Include screenshots of each request and response in your submission.

Optional Frontend Demo
Open index.html in a browser

Fetches all snippets and displays them:

html
Copy code
<script>
fetch("http://localhost:3000/api/snippets")
  .then(res => res.json())
  .then(data => console.log(data));
</script>
Reflection (200–300 words)
This project taught me how to design and implement a full-stack RESTful API. I learned to structure a Node.js project with Express and MongoDB, define data schemas with Mongoose, and handle requests safely using query parameters. Testing with Postman reinforced my understanding of HTTP methods and JSON data.

Additionally, I learned the importance of security by using .gitignore and .env files to protect sensitive credentials. Deploying the backend on Render exposed me to real-world hosting environments and the process of connecting a live server to a database.

I also experimented with creating a minimal frontend using vanilla HTML and JavaScript, demonstrating how a frontend can consume a backend API. Overall, this project improved my ability to integrate multiple technologies and gave me practical experience that will apply to any real-world web development task.

Self-Assessment Against Rubric
Criteria	Self-Assessment
Functionality	All required API endpoints are implemented, tested, and working.
Code Quality	Code is organized, commented, and follows consistent naming conventions.
Security	.env used for sensitive data, .gitignore in place to avoid committing secrets.
Documentation	README.md contains installation, run steps, API docs, screenshots, reflection, and self-assessment.
Deployment	Project deployed on Render; public URL is working.
Testing	API tested using Postman; screenshots included.

Screenshots
Include images of Postman requests/responses for each endpoint:

Create Snippet (POST)

Get All Snippets (GET)

Filter by Language (GET)

Get One Snippet (GET)

Demo Video
Link: [Insert your 3–5 minute demo video link here]

Live Deployment
Render Web Service URL: https://codesnippet-project.onrender.com

GitHub Repository
Repository URL: https://github.com/Mariamajaks/Codesnippet_project