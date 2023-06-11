<b>Hobbie Application</b>
<hr>

This project is a full-stack web application built using ReactJS and Spring Boot. It consists of two applications: a Spring Boot backend called `spring-backend` and a ReactJS frontend called `react-frontend`.

<b>Description</b>
<hr>

The project focuses on creating a service-oriented platform that connects consumers and small businesses in the Arts, Entertainment, and Recreation sector.

<b>Applications</b>
<hr>

<b> - Spring Backend</b>

The `spring-backend` is a Java backend application built with Spring Boot. It provides a REST API to manage hobbies and requires authentication using an access token (JWT) to access secured endpoints. The backend stores its data in a MySQL database. 

The `spring-backend` includes the following endpoints:

- Explore the API documentation: [http://localhost:8080/v3/api-docs](http://localhost:8080/v3/api-docs)
- Swagger UI for API exploration: [http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)

<b> - React Frontend</b>

The `react-frontend` is a frontend application developed with ReactJS. It allows users to discover and save hobbies, and businesses can manage offers. Users and businesses need to log in with their username and password to access the application. The frontend communicates with the secured endpoints in the `spring-backend` using an access token (JWT). The UI styling is implemented using the Semantic UI React framework.

<b>Prerequisites</b>
<hr>

- Java 11+
- Node.js and npm
- JWT (JSON Web Token)

<b>Setup Instructions</b>
<hr>

1. Clone the repository:

   ```bash
   git clone https://github.com/praveenkumar-236.git
   ```

2. Frontend Setup:
   - Install Node.js and npm (Node Package Manager).
   - Navigate to the `react-frontend` subfolder:

     ```bash
     cd react-frontend
     ```

   - Install the required modules:

     ```bash
     npm install
     ```

   - Start the frontend application on your local machine:

     ```bash
     npm start
     ```

   - Access the application in your web browser at [http://localhost:4200](http://localhost:4200).

3. Backend Setup:
   - Install JDK 11.0.11 and ensure Docker is installed (version 20.10.7) along with Docker Compose (version 1.8.0).
   - Navigate to the `spring-backend` subfolder:

     ```bash
     cd spring-backend
     ```

   - Run the project using Docker Compose:

     ```bash
     docker-compose up --build
     ```

   - The backend will be accessible at [http://localhost:8080](http://localhost:8080).

<b>Important Note</b>
<hr>

Make sure to configure the `spring.mail.username` and `spring.mail.password` properties in the `application.properties` file to enable sending email confirmations for updating user entries. Without valid mail credentials, the application may encounter a `javax.mail.AuthenticationFailedException`, but the rest of the application should work normally.

Feel free to customize the application based on your specific project requirements and add additional features as needed.

<b>License</b>
<hr>

[MIT License](LICENSE)