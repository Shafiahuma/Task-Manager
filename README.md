# Task-Manager

- **Frontend**:
  - React.js
  - HTML/CSS
  - JavaScript

- **Backend**:
  - Node.js
  - Express.js
  - PostgreSQL
  
- **APIs**:
  - RESTful API architecture


## Getting Started

To run the app, follow these steps:

### Prerequisites

- Node.js must be installed on your local machine
- PostgreSQL must installed on your local machine

### Installation

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
   - ```npm start```
5. To run the "server" side:
   - ```cd backend```
   - ```npm init -y```
   - ```npm install express pg cors body-parser```
   - ```node index.js```
