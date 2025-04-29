## Student Database Management System#
This project is a CRUD (Create, Read, Update, Delete) API built with Node.js, Express, and MongoDB to manage student records efficiently.

## Features
Add a new student record

Retrieve all student records

Update student details

Delete a student record

## Prerequisites
Ensure the following are installed on your system:

Node.js (v14 or higher)

MongoDB (local or Atlas)

Installation
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
cd student-database-api
2. Install Dependencies
bash
Copy
Edit
npm install
## 3. Set Up MongoDB
Use a local MongoDB or create a MongoDB Atlas cluster.

Update the MongoDB connection URI in .env or server.js.

## 4. Run the Server
bash
Copy
Edit
npm start
The API will start on http://localhost:3000 (or your specified port).

## API Endpoints
1. Create a New Student
Endpoint: POST /students
Request Body:

json
Copy
Edit
{
  "name": "John Doe",
  "email": "john@example.com",
  "rollNumber": "S1234",
  "course": "Computer Science",
  "age": 20
}
Response:

json
Copy
Edit
{
  "message": "Student added successfully",
  "student": {
    "_id": "xyz123",
    "name": "John Doe",
    "email": "john@example.com",
    "rollNumber": "S1234",
    "course": "Computer Science",
    "age": 20
  }
}
2. Get All Students
Endpoint: GET /students

Response:

json
Copy
Edit
[
  {
    "_id": "xyz123",
    "name": "John Doe",
    "email": "john@example.com",
    "rollNumber": "S1234",
    "course": "Computer Science",
    "age": 20
  }
]
3. Update Student Details
Endpoint: PUT /students/:id
Request Body:

json
Copy
Edit
{
  "email": "john.doe@university.edu",
  "course": "AI and Data Science"
}
Response:

json
Copy
Edit
{
  "message": "Student updated successfully",
  "updatedStudent": {
    "_id": "xyz123",
    "email": "john.doe@university.edu",
    "course": "AI and Data Science"
  }
}
4. Delete a Student
Endpoint: DELETE /students/:id
Response:

json
Copy
Edit
{
  "message": "Student deleted successfully"
}
Project Structure
bash
Copy
Edit
student-database-api/
│── models/
│   └── student.js         # Mongoose schema for Student
│── routes/
│   └── studentRouter.js        # CRUD routes for student operations
│── index.js              # Entry point of the app
│── .env                   # MongoDB URI, PORT config
│── package.json           # Project metadata & dependencies
│── README.md              # Project documentation
Dependencies
express – Web framework for Node.js

mongoose – ODM for MongoDB

dotenv – Environment variable loader

nodemon – Auto-reload server during development (devDependency)

Testing the API
Tools:
Postman – For API request testing

curl – CLI tool for testing endpoints

Example cURL:
bash
Copy
Edit
curl -X GET http://localhost:3000/students
License
This project is licensed under the MIT License.
Feel free to use, modify, and distribute it.
