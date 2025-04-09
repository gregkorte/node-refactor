# Books

1. Fundamentals
Introduction to Node.js: Overview, installation, basic concepts.
JavaScript Basics: ES6+ features, asynchronous programming.
2. Core Concepts
HTTP Server: Using the http module.
File System: Reading/writing files with the fs module.
Modules: Creating and importing modules.
3. Web Development
Express.js: Setting up a server, routing, middleware.
RESTful APIs: Building and consuming APIs.
4. Databases
SQL and NoSQL: Connecting to databases (PostgreSQL, MongoDB).
ORMs: Using Sequelize or Mongoose.
5. Advanced Topics
Security: Common vulnerabilities, secure coding practices.
Testing: Writing tests with Mocha and Chai.
Performance: Optimizing Node.js applications.
6. Capstone Project
Full Application: Developing a complete application using Node.js, Express, and a database.
Deployment: Deploying the application to a cloud service.
7. Additional Resources
Community and Support: Node.js community resources, forums, and documentation.

# Book 1 - Fundamentals :nut_and_bolt: :wrench:

The purpose of this book is to provide a basic introduction to the syntax of JavaScript and the structure of Node.js programs.

## Learning Objectives

1. JavaScript syntax
    <ul>
        <li>Variables and data types</li>
        <li>Control flow: loops, conditions, boolean</li>
        <li>Collections: Array, Object</li>
    </ul>
1. Asynchronous Programming
    <ul>
        <li>Callbacks</li>
        <li>Promises</li>
        <li>async/await</li>
    </ul>
1. Node.js Fundamentals
    <ul>
        <li>Introduction to Node.js</li>
        <li>Using core modules</li>
        <li>Creating an HTTP server</li>
    </ul>

## Table of Contents

<!-- prettier-ignore-start -->

### Installations
|[Installations for Book 1](./chapters/book-1-installations.md) :computer:|
|--|

Start on the top left, and work your way down. When you get to the bottom, continue at the top of the column immediately to the right.
|#|Intro to Node.js <br>:football::curly_loop: <sub>(guided tour)</sub>|JavaScript Basics :pencil2:|Node.js Essentials <br> :file_folder:|
|:-:|:-:|:-:|:-:|
|1|[Setting up Node.js](./chapters/setting-up-nodejs.md)|[JavaScript Variables](./chapters/js-variables.md)|[Using Core Modules](./chapters/using-core-modules.md)|
|2|[Node.js Architecture](./chapters/nodejs-architecture.md)|[Data Types](./chapters/js-data-types.md)|[File System Module](./chapters/file-system-module.md)|
|3|[NPM Basics](./chapters/npm-basics.md)|[Control Flow](./chapters/js-control-flow.md)|[Creating HTTP Servers](./chapters/http-servers.md)|
|4|[Creating a Simple Server](./chapters/creating-simple-server.md)|[Loops](./chapters/js-loops.md)|[EventEmitter](./chapters/event-emitter.md)|
|5|[Debugging Node.js](./chapters/debugging-nodejs.md)|[Arrays and Objects](./chapters/js-arrays-objects.md)|[Async Programming](./chapters/async-programming.md)|
|6|[Node.js Modules](./chapters/nodejs-modules.md)|[Functions](./chapters/js-functions.md)|||
|7|[Error Handling](./chapters/error-handling.md)|[Promises](./chapters/js-promises.md)|||
|8|[HTTP Methods](./chapters/http-methods.md)|[async/await](./chapters/js-async-await.md)|||

### Assessment
| Link |
|------|
| [Assessment for Fundamentals](#) |

|:compass: Explorer Chapters (after you finish the table above)|
|--|
|:pencil2: [Advanced JavaScript](./chapters/advanced-js.md)|
|:file_folder: [Debugging Techniques](./chapters/debugging-techniques.md)|
|:pencil2: [Creating Custom Modules](./chapters/creating-custom-modules.md)|

|:test_tube: Projects|
|--|
|[Simple HTTP Server](./chapters/simple-http-server.md)|
|[File System Explorer](./chapters/file-system-explorer.md)|
<!-- prettier-ignore-end -->



> Prompts: Let's assume students have already been through a three month course which taught them basic to intermediate understanding of html, css and javascript. Assume they have learned the following concepts:
 - data types
 - methods
 - object manipulation
 - modularization
 - functions
 - react
 - react dom
 - json-server
> Now pick up where that course left off and introduce Node.js to them with the end goal in three months being to build a full stack application using either react, next, vue or angular.


Got it! Let’s adjust the program to focus on building a full-stack application with the required CRUD operations, relationships, and user-specific data by the end of the course. We'll ensure the progression is gradual, focusing on building essential skills before tackling more complex concepts.

Here's the revised outline:

# Full-Stack Development Course Outline

## Book 1: Introduction to Node.js and Backend Fundamentals

### Learning Goals:
- Understand the basics of Node.js and its ecosystem.
- Learn how to set up a Node.js project.
- Master fundamental backend concepts like routing, middleware, and databases.
- Gain hands-on experience with Express.js, a popular Node.js framework.

### Chapters:
#### Chapter 1: Getting Started with Node.js
- **Guided Tour:** Setting up Node.js and NPM, creating a simple server.
  - **Task 1:** Install Node.js and NPM.
  - **Task 2:** Create a simple "Hello World" server.
  - **Task 3:** Understand basic routing.

#### Chapter 2: Building with Express.js
- **Project:** Develop a simple API with Express.js.
  - **Task 1:** Set up an Express.js project.
  - **Task 2:** Create routes and handle requests.
  - **Task 3:** Implement middleware for logging and error handling.

#### Chapter 3: Working with Databases
- **Project:** Connect an Express.js application to a database (SQLite or MongoDB).
  - **Task 1:** Set up SQLite or MongoDB.
  - **Task 2:** Create models and schemas.
  - **Task 3:** Implement CRUD operations.

#### Chapter 4: Building a RESTful API
- **Project:** Create a RESTful API for a simple resource (e.g., a blog).
  - **Task 1:** Define API endpoints.
  - **Task 2:** Implement the endpoints with proper HTTP methods.
  - **Task 3:** Test the API using Postman or similar tools.

### Assessment:
- Build a small RESTful API project from scratch with CRUD operations and database integration.

### Further Exploration:
- **Authentication and Authorization**
  - Implement JWT authentication.
  - **Task:** Add user login and registration to the API.

### Group Project:
- Develop a more complex API (e.g., a task management system) with user authentication and role-based access control.

## Book 2: Building a Basic Full-Stack Application

### Learning Goals:
- Integrate a Node.js backend with a frontend framework (React, Vue, Angular).
- Understand full-stack development principles and best practices.
- Implement CRUD operations from the frontend to the backend.

### Chapters:
#### Chapter 1: Setting Up the Frontend
- **Guided Tour:** Setting up React, Vue, or Angular.
  - **Task 1:** Choose a frontend framework.
  - **Task 2:** Set up a basic project.
  - **Task 3:** Connect the frontend to the Node.js backend.

#### Chapter 2: Creating Full-Stack CRUD Features
- **Project:** Implement a simple CRUD feature (e.g., a to-do list).
  - **Task 1:** Create frontend components.
  - **Task 2:** Implement API calls to the backend.
  - **Task 3:** Handle data on the frontend and backend.

#### Chapter 3: User Authentication
- **Project:** Add user authentication to the full-stack application.
  - **Task 1:** Implement login and registration on the frontend.
  - **Task 2:** Handle authentication on the backend.
  - **Task 3:** Protect routes and manage user sessions.

#### Chapter 4: One-to-Many Relationships
- **Project:** Implement a one-to-many relationship (e.g., users and posts).
  - **Task 1:** Define relationships in the database.
  - **Task 2:** Implement related CRUD operations.
  - **Task 3:** Display related data on the frontend.

### Assessment:
- Build a full-stack application with user authentication and a one-to-many relationship.

### Further Exploration:
- **Authorization and Role Management**
  - Implement role-based access control.
  - **Task:** Add admin and user roles to the application.

### Group Project:
- Develop a full-stack application with user authentication and a one-to-many relationship, including role-based access control.

## Book 3: Intermediate Full-Stack Development

### Learning Goals:
- Deepen understanding of full-stack development.
- Implement many-to-many relationships.
- Enhance application with additional features and optimizations.

### Chapters:
#### Chapter 1: Many-to-Many Relationships
- **Guided Tour:** Implement a many-to-many relationship (e.g., users and groups).
  - **Task 1:** Define many-to-many relationships in the database.
  - **Task 2:** Implement related CRUD operations.
  - **Task 3:** Display many-to-many data on the frontend.

#### Chapter 2: Advanced CRUD Operations
- **Project:** Enhance CRUD operations with additional features (e.g., pagination, search).
  - **Task 1:** Implement pagination on the backend and frontend.
  - **Task 2:** Add search functionality.
  - **Task 3:** Optimize data fetching and performance.

#### Chapter 3: User-Specific Data
- **Project:** Manage user-specific data (e.g., user profiles, personalized settings).
  - **Task 1:** Implement user-specific data storage.
  - **Task 2:** Create user-specific views and forms.
  - **Task 3:** Handle user-specific data securely.

#### Chapter 4: Deployment and Best Practices
- **Project:** Deploy the full-stack application to a cloud provider (e.g., Heroku, Vercel).
  - **Task 1:** Set up a deployment pipeline.
  - **Task 2:** Configure environment variables and secrets.
  - **Task 3:** Monitor and maintain the deployed application.

### Assessment:
- Build and deploy a full-stack application with many-to-many relationships and user-specific data.

### Further Exploration:
- **State Management**
  - Implement state management in the frontend framework (e.g., Redux, Vuex).
  - **Task:** Integrate state management into the existing application.

### Group Project:
- Develop a full-featured application with many-to-many relationships, user-specific data, and advanced CRUD features, then deploy it.

## Book 4: Capstone Project and Advanced Topics

### Learning Goals:
- Apply all the learned concepts to build a comprehensive full-stack application.
- Explore advanced topics and tools to enhance the application.
- Collaborate on a complex project and prepare for real-world development.

### Chapters:
#### Chapter 1: Capstone Project Planning
- **Guided Tour:** Plan and design a capstone project.
  - **Task 1:** Define project scope and requirements.
  - **Task 2:** Design the database schema.
  - **Task 3:** Create wireframes and user stories.

#### Chapter 2: Building the Capstone Project
- **Project:** Develop the capstone project incrementally.
  - **Task 1:** Set up the backend and frontend.
  - **Task 2:** Implement core features (CRUD, authentication, relationships).
  - **Task 3:** Test and debug the application.

#### Chapter 3: Enhancing the Capstone Project
- **Project:** Add advanced features and optimizations.
  - **Task 1:** Implement additional features (e.g., real-time updates, file uploads).
  - **Task 2:** Optimize performance and scalability.
  - **Task 3:** Improve UI/UX and accessibility.

#### Chapter 4: Finalizing and Deploying the Capstone Project
- **Project:** Prepare the capstone project for deployment.
  - **Task 1:** Conduct thorough testing and code review.
  - **Task 2:** Deploy the application.
  - **Task 3:** Present the project to peers and instructors.

### Assessment:
- Complete and deploy the capstone project, demonstrating all the learned skills.

### Further Exploration:
- **Explore DevOps Practices**
  - Implement CI/CD pipelines and automated testing.
  - **Task:** Set up a CI/CD pipeline for the capstone project.

### Group Project:
- Collaborate on a complex full-stack application, integrating all the skills learned throughout the course, and present it as a final project.

---
# Node ORMs
    Sequelize
    TypeORM
    Mongoose (TypeGoose)
    Prisma

---
# Testing
    Jest (Compatible with NodeJS, React, Angular, VueJS)
    Mocha
    Jasmine

---

# Stack Notes

### MEAN (YouTube)
    Mongo, Express, Angular, Node

### MERN (Netflix)
    Mongo, Express, React, Node

### MEVN (Alibaba)
    Mongo, Express, Vue, Node

### LAMP (WordPress)
    Linux, Apache, MySQL, PhP

### ROR (AirBnB)
    Ruby on Rails

### ASP.NET (Stack Overflow)
    C#, F#, Visual Basic

### Python-Django (Pixar)
    Python, Django

### Flutter for Web (Google Ads)
    Dart

### React Native (Facebook)
    React Native, iOS, Android

### Java EE (Tesla)
    Java Enterprise

### Serverless (Figma)
    AWS Lambda, Google Cloud Functions, Azure Functions

### Other Javascript Frameworks
    Next.js
    Vue.js
    Svelte
    NestJS
    NuxtJS
    Gatsby




