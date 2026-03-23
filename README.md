Blog Management API - TAF 1 (INF222)

Description

This project is a RESTful Backend API designed to manage blog articles, developed for the INF222 - EC1 (Backend Development) course. The application facilitates full CRUD (Create, Read, Update, Delete) operations for a simple blog system and was built following a structured learning path on the CleeRoute platform.

Technical Stack

Runtime Environment: Node.js

Framework: Express.js

Database: SQLite / MySQL / MongoDB

Documentation: Swagger (OpenAPI 3.0)

Architecture

The application implements a clear separation of concerns to ensure maintainability:

Routes: Defines the API endpoints and maps them to controllers.

Controllers: Contains the business logic and processes incoming requests.

Models: Manages data structures and database interactions.

Installation and Setup

Prerequisites

Node.js (v14 or higher)

npm (Node Package Manager)

Step 1: Clone the Repository

git clone [https://github.com/mikellechanyon/blog-api.git](https://github.com/mikellechanyon/blog-api.git)
cd blog-api


Step 2: Install Dependencies

npm install


Step 3: Configuration

Ensure your environment variables are configured in a .env file if required by your specific database setup. By default, the API runs on port 3000.

Step 4: Start the Server

npm start


The server will be accessible at http://localhost:3000.

API Documentation

Endpoints

The following endpoints implement the functionalities required in the TAF 1 specifications:

Method

Endpoint

Description

Status Codes

POST

/api/articles

Create a new article

201, 400

GET

/api/articles

Retrieve all articles (supports filtering)

200

GET

/api/articles/:id

Retrieve a specific article by ID

200, 404

PUT

/api/articles/:id

Update an existing article

200, 400, 404

DELETE

/api/articles/:id

Remove an article from the database

200, 404

GET

/api/articles/search

Search titles/content via ?query=text

200

Data Model

Articles consist of the following fields:

titre: String (Required)

contenu: String (Required)

auteur: String (Required)

date: String (ISO format)

categorie: String

tags: Array of Strings

Validation and Error Handling

The API implements robust validation and uses standard HTTP status codes:

200 OK: Request succeeded.

201 Created: Resource successfully created.

400 Bad Request: Missing required fields or malformed JSON.

404 Not Found: Resource with the specified ID does not exist.

500 Internal Server Error: Unexpected server-side issues.
