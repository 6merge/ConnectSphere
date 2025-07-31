<b>ConnectSphere</b>  
<hr>

This project consists of two applications: one is a Spring Boot REST API  
called `spring-backend`, and another is a ReactJS application called  
`react-frontend`.

ConnectSphere is a service-oriented platform focused on establishing and maintaining  
connections between consumers and small businesses in the Arts,  
Entertainment, and Recreation sector.

<b>Applications</b>  
<hr>

<b>- spring-backend</b>  
Spring Boot Web Java backend application that exposes a REST API to  
manage hobbies. Its secured endpoints can only be accessed if an access  
token (JWT) is provided.

The backend stores its data in a MySQL database and includes endpoints for user/business registration, authentication, and CRUD operations.

<b>- react-frontend</b>  
ReactJS frontend application where users can discover and save hobbies, while businesses can manage their offers.  
Access requires user/business login using username and password.  
All requests to secured backend endpoints are authorized using a JWT token  
generated upon successful login.

The frontend uses Semantic UI React for styling.

<b>Prerequisites</b>  
<hr>

- Java 11+  
- npm  
- JWT  

<b>Set up</b>  
<hr>

Clone the repository:

<pre>git clone [your repository link here]</pre>

Navigate to the project folder:

<pre>cd ConnectSphere</pre>

<b>Frontend -</b>  
Install Node.js v16.13.1 and npm v8.3.0

Navigate to the frontend:

<pre>cd react-frontend</pre>

Install dependencies:

<pre>npm install</pre>

Start the frontend server:

<pre>npm start</pre>

App runs on:  
<pre>http://localhost:4200</pre>

<b>Backend -</b>  
Install JDK 11.0.11  
Install Docker v20.10.7  
Install Docker Compose v1.8.0

Navigate to the backend:

<pre>cd spring-backend</pre>

Start backend services:

<pre>docker-compose up --build</pre>

App runs on:  
<pre>http://localhost:8080</pre>

Explore backend APIs at `/v3/api-docs` and Swagger UI at `/swagger-ui/index.html`

<b>Authentication Flow</b>  
- Use `/signup` to create a client-user  
- Use `/register` to create a business-user  
- Use `/authenticate` to obtain a JWT token  
- Use the JWT token to access secured endpoints

<b>Spring Mail (Optional)</b>  
To enable email functionality (e.g., confirmation emails), add the following in `application.properties`:

