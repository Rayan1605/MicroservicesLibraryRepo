# Library Management System Overview

This project is a **Library Management System** built with **Spring Boot**, utilizing **Spring Security** for user authentication and role management, and **JPA** for database interactions (working with MySQL or other relational databases).

## Main Features:

1. **User Login & Roles (Spring Security)**:
  - **Spring Security** is used to manage user roles such as:
    - **Admin**: Full access to manage users, books, and settings.
    - **Librarian**: Can manage book inventory and borrowing/returning of books.
    - **Member**: Can browse, borrow, and return books.
  - **JWT tokens** are used for authentication, enabling secure API interactions after login.

2. **Managing Books (JPA)**:
  - The system allows for adding, updating, deleting, and searching for books.
  - **JPA** handles database interactions seamlessly, allowing for easy management of book records.
  - Users can search for books based on title, author, or category.

3. **Borrowing & Returning Books**:
  - Users can borrow and return books, and each transaction is tracked for accountability.
  - This feature leverages **JPA** to map relationships between users and books, making it easy to track borrowing history.

4. **Roles & Permissions**:
  - Admins have full control over users and books, while librarians handle day-to-day operations.
  - Members can only access book-browsing and borrowing functionality.

5. **Using Docker**:
  - The entire system is containerized using **Docker**, ensuring easy deployment across different environments.

6. **REST API**:
  - The system exposes a **REST API** for external applications to interact with (e.g., mobile apps or front-end).
  - All APIs are secured using **JWT tokens**, ensuring only authenticated users can access certain functionalities.

---

## Microservices Architecture:

This project follows a **microservice architecture** and is divided into several independent services, each responsible for specific functionality. These services interact through **REST APIs** and are containerized using **Docker** for easy deployment and scaling.

### Repositories for the Back-end::

- [ReviewRepository](https://github.com/Rayan1605/ReviewRepository)  
  Handles all operations related to user reviews, including CRUD operations and ratings.

- [PaymentService](https://github.com/Rayan1605/PaymentService)  
  Manages payment processing, gateways, and transaction records.

- [MessageService](https://github.com/Rayan1605/MessageService)  
  Provides messaging services, including notifications and chat.

- [BookService](https://github.com/Rayan1605/BookService)  
  Core service for managing books, including cataloging, availability, and rentals.

- [AdminService](https://github.com/Rayan1605/AdminService)  
  Admin panel services to manage books, user roles, and access control.

---

## Frontend

The front-end part of the project, located in the [FrontEndLibraryProject](https://github.com/Rayan1605/FrontEndLibraryProject), is built with **React**. It connects to the backend services for various functions like user login, book management, and borrowing books.

- **React**: Used for building the user interface.
- **API Integration**: Frontend interacts with backend services using **Axios** to make API requests.
- **JWT Authentication**: Secures API communication by attaching tokens to each request.
- **Component-Based Architecture**: Components like **Login**, **BookList**, and **BorrowedBooks** provide modular, reusable parts of the UI.

---

## Technologies Used:

- **Spring Boot**: Backend framework used for building microservices.
- **Spring Security**: For managing authentication and user roles.
- **Spring Data JPA**: For interacting with the MySQL database.
- **JWT**: Used for token-based authentication.
- **Docker**: For containerization of microservices.
- **React**: For building the front-end user interface.
- **Axios**: For making HTTP requests from the front-end to backend services.
---


This is a complete, scalable library management system using modern development practices and technologies.


