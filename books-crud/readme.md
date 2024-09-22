This is a full-stack web application built using Node.js and React.js. The backend is powered by Express and MySQL, allowing users to perform CRUD operations (Create, Read, Update, Delete) on a collection of books. The frontend, built with React, interacts with the backend to display and manage book data.

Features
View all books in the database.
Add new books with title, description, price, and cover.
Edit existing books.
Delete books.
Tech Stack
Frontend: React.js
Backend: Node.js, Express.js
Database: MySQL
Other Libraries: CORS, MySQL, Express
Prerequisites
Before running this project, make sure you have:

Node.js and npm installed. You can download them from Node.js official website.
MySQL installed and running on your system.
Getting Started

2. Install dependencies for both frontend and backend
Navigate to both frontend and backend directories and install the required packages.

For Backend:

bash

cd backend
npm install
For Frontend:

bash

cd frontend
npm install
3. Set up the MySQL Database
Start MySQL server.
Create a database named test.
Run the following SQL script to create the books table:
sql

CREATE DATABASE test;

USE test;

CREATE TABLE books (
  id INT AUTO_INCREMENT PRIMARY KEY,
  title VARCHAR(255),
  `desc` TEXT,
  price DECIMAL(10, 2),
  cover VARCHAR(255)
);
4. Configure the Backend
Ensure your MySQL credentials are correct in the backend file.

js

const db = mysql.createConnection({
  host: "localhost",
  user: "root",
  password: "YOUR_PASSWORD",
  database: "test",
});
5. Running the Backend
Once you've set up the MySQL database and configured the connection, you can start the backend server.

bash

cd backend
npm start
The backend will be running on http://localhost:8800.

6. Running the Frontend
To start the React frontend, navigate to the frontend folder and start the development server.

bash

cd frontend
npm start
The React frontend will be running on http://localhost:3000.

API Endpoints
Here are the available endpoints for the backend:

GET /books: Retrieves all books from the database.
POST /books: Adds a new book to the database. Requires title, desc, price, and cover in the request body.
DELETE /books/
: Deletes a book by its id.
PUT /books/
: Updates a book's details. Requires title, desc, price, and cover in the request body.
Example of a book object:
json

{
  "title": "The Great Gatsby",
  "desc": "A novel by F. Scott Fitzgerald",
  "price": 19.99,
  "cover": "https://example.com/gatsby.jpg"
}
Folder Structure
java

book-management-app/
│
├── backend/
│   ├── node_modules/
│   ├── package.json
│   ├── index.js (your backend file)
├── frontend/
│   ├── node_modules/
│   ├── public/
│   ├── src/
│   ├── package.json
├── README.md
License
This project is licensed under the MIT License - see the LICENSE file for details.

Bu README dosyası, projenin amacını, kurulum adımlarını ve nasıl çalıştığını aç