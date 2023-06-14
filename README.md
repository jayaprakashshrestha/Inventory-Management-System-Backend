# Inventory Management System (Backend)

This is the backend component of an Inventory Management System (IMS) developed using Java and Spring Boot framework. The backend handles various API endpoints to perform CRUD operations on items in the inventory and manage user authentication.

## Prerequisites

Before running the application, ensure that you have the following installed:

- Java Development Kit (JDK) 8 or later
- Apache Maven (for dependency management)

## Getting Started

To set up the project locally, follow these steps:

1. Clone the repository to your local machine.
2. Open the project in your preferred IDE.
3. Build the project using Maven to fetch the required dependencies.
4. Configure the database connection details in the `application.properties` file.
5. Run the application.

## Project Structure

The project follows a standard Maven project structure. The main components are as follows:

- `com.example.ims.Controller`: Contains the controller classes responsible for handling incoming HTTP requests.
- `com.example.ims.Model`: Defines the data models used in the application.
- `com.example.ims.Service`: Implements the business logic and interacts with the database.
- `com.example.ims.Repository`: Provides the repository interfaces for database operations.
- `resources`: Contains the application properties and configuration files.

## API Endpoints

The following API endpoints are available:

### Inventory Endpoints

- `GET /items`: Retrieves a list of all items in the inventory.
- `GET /items/{id}`: Retrieves details of a specific item by ID.
- `POST /item`: Adds a new item to the inventory.
- `PUT /items/{id}`: Updates an existing item by ID.
- `DELETE /items/{id}`: Deletes an item from the inventory by ID.
- `PUT /items/{id}/dispatch`: Dispatches a specific quantity of an item.

### User Endpoints

- `POST /login`: Validates user credentials and generates a session ID.
- `GET /users`: Retrieves a list of all users.
- `POST /user`: Creates a new user.

## Database

The application uses a MongoDB database to store item and user information. Ensure that you have MongoDB installed and running, and update the `application.properties` file with the appropriate database connection details.

## Authentication and Session Management

User authentication is implemented using a username and password combination. Upon successful login, a unique session ID is generated and stored as a cookie in the client's browser. This session ID is required to access protected endpoints.

## Error Handling

The backend handles various error scenarios and returns appropriate HTTP response codes along with error messages in the response body. The frontend should handle these error responses gracefully.

## Cross-Origin Resource Sharing (CORS)

The backend is configured to allow Cross-Origin Resource Sharing (CORS) requests. This enables the frontend, running on a different domain or port, to communicate with the backend APIs.

## Future Enhancements

The following are some potential areas for future enhancements:

- Implementing user roles and access control for different user types (admin, regular user, etc.).
- Adding pagination and sorting options for retrieving items.
- Implementing additional search and filtering capabilities for items.
- Integrating third-party APIs for real-time inventory updates.
- Implementing additional authentication mechanisms (e.g., OAuth2) for enhanced security.

## Acknowledgments

Special thanks to the developers and contributors of the libraries and frameworks used in this project.Happy Coding! Learn Coding!
