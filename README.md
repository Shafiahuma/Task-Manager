# Task Management Web Application

## Overview

This project is a web application designed to help users manage a list of tasks. It features a front-end interface for user interaction and a back-end server to handle data storage and retrieval. Users can add, edit, delete, and mark tasks as completed or not completed. The application is built with a modern front-end framework and a RESTful API on the back-end, ensuring a responsive and user-friendly experience on both desktop and mobile devices.

### Features

- Display a list of tasks with titles, descriptions, and completion statuses.
- Add new tasks with a title and description.
- Edit existing tasks.
- Delete tasks.
- Mark tasks as completed or not completed.
- Fully responsive design for desktop and mobile

### Technologies Used
- Front-End: React
- Back-End: Node.js with Express 
- Database: PostgreSQL
- CSS: Bootstrap

## Getting Started

To run the app, follow these steps:

### Prerequisites

- Node.js must be installed on your local machine
- PostgreSQL must installed on your local machine

### Instructions on how to set up and run the project locally.

1. Download the repository.
2. After downloading, you have to make a change to make the database work.
   - In that index.js file, replace the "user, password, host, port, database" according to your own machine's postgreSQL's credentials.
   - Create a database using the followiong commands:
   - ```CREATE DATABASE task_manager```
   - ```CREATE TABLE tasks ( id SERIAL PRIMARY KEY, title VARCHAR(255) NOT NULL, description TEXT NOT NULL, status BOOLEAN NOT NULL DEFAULT false);```
3. Both the "frontend" and "backend" sides should be run in the terminal to make the web application work.
4. To run the "frontend" side, in the terminal, run these: 
   - ```cd frontend```
   - ```npm install```
   - ```npm install bootstrap```
   - ```npm install axios```
   - ```npm install react-bootstrap bootstrap```
   - ```npm start```
5. To run the "server" side:
   - ```cd backend```
   - ```npm init -y```
   - ```npm install express pg cors body-parser```
   - ```node index.js```

## API Endpoints
### Task Management API

- GET /tasks
  Description: Retrieve a list of tasks.
  Response: JSON array of tasks.

- GET /tasks:id
  Description: Retrieve a specific task by ID.
  Parameters: id - The ID of the task.
  Response: JSON object of the task.

- POST /tasks
  Description: Create a new task.
  Request Body: JSON object with title, description and status fields.
  Response: JSON object of the created task.

- PUT /tasks:id
  -- Description: Update an existing task by ID.
  -- Parameters: id - The ID of the task.
  -- Request Body: JSON object with title, description, and completed fields.
  -- Response: JSON object of the updated task.
  
- DELETE /tasks:id
  Description: Delete a task by ID.
  Parameters: id - The ID of the task.
  Response: JSON object of the deleted task.

All the API endpoints are evaluated using postman software before using it in frontend.
