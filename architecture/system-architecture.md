# System Architecture – Manager Library

## 1. Introduction

This document describes the high-level architecture of Manager Library, including its main components, responsibilities, and communication flows.

The architecture is based on a client-server model in which the frontend communicates with the backend through an HTTP API, while the backend manages business logic and database operations.

## 2. Architectural Overview

Manager Library follows a layered architecture composed of three main layers:

1. **Presentation Layer:** Provides the user interface and allows users to interact with the system.
2. **Application Layer:** Processes requests, applies business rules, manages authentication, and coordinates operations.
3. **Data Layer:** Stores and manages the information required by the application.

## 3. Main System Components

### 3.1 Frontend

The frontend is developed using React and is responsible for presenting the system interface.

Its main responsibilities include:

- Displaying the application screens.
- Allowing administrators and librarians to interact with the system.
- Sending HTTP requests to the backend API.
- Displaying information received from the backend.
- Managing the user interface according to authentication and authorization states.

### 3.2 Backend

The backend is developed using PHP with Laravel.

Its main responsibilities include:

- Exposing the system's HTTP API endpoints.
- Processing client requests.
- Applying business rules and validations.
- Managing user authentication through JWT.
- Enforcing role-based access control.
- Managing books, categories, members, loans, and returns.
- Coordinating database transactions.
- Generating reports and queries.

### 3.3 Database

The system uses PostgreSQL 16 as its database management system.

The database uses the `library` schema and stores information related to:

- Users.
- Categories.
- Books.
- Members.
- Loans.
- Loan items.

The database maintains the relationships and integrity of the information managed by the application.

## 4. Component Communication

The main communication flow is described below:

1. An administrator or librarian interacts with the React frontend.
2. The frontend sends an HTTP request to the Laravel backend.
3. The backend validates the request and checks authentication and authorization when required.
4. The application processes the corresponding business rules.
5. The backend performs the necessary database operations through PostgreSQL.
6. The backend returns an HTTP response to the frontend.
7. The frontend displays the result to the user.

## 5. Authentication and Authorization

Manager Library uses JSON Web Tokens (JWT) for authentication.

The authentication and authorization process includes:

- Administrators and librarians authenticate using their credentials.
- The system issues a JWT after successful authentication.
- The token has a validity period of 8 hours.
- Protected endpoints require a valid authentication token.
- Access to operations is controlled according to the user's assigned role.

Library members are registered in the system but do not authenticate through the application, according to the project specification.

## 6. Main Business Modules

The system is organized around the following functional modules:

| Module | Responsibility |
|---|---|
| Authentication | Manages user authentication and JWT validation. |
| User Management | Manages administrator and librarian accounts and roles. |
| Category Management | Provides the predefined categories used to classify books. |
| Book Management | Manages the library catalog and book availability. |
| Member Management | Registers and manages library members. |
| Loan Management | Registers loans and validates loan conditions. |
| Return Management | Processes individual book returns and updates availability. |
| Reports | Provides overdue loan information and most borrowed book reports. |

## 7. Data Consistency

The architecture must preserve data consistency during operations involving related records.

In particular:

- Loan registration and book availability updates must occur within the same database transaction.
- A loan item must not be returned more than once.
- Loan and return history must be preserved.
- Relationships between books, members, loans, and loan items must remain consistent.

## 8. External Repository Organization

The project is organized into six repositories, each with a specific responsibility:

- **Docs:** Central project specifications and technical documentation.
- **API:** Backend application based on Laravel.
- **App:** Frontend application based on React.
- **Page:** Public presentation website.
- **Infra:** Infrastructure configuration and database environment.
- **Tool:** Utilities and demonstration data seeding.

Each repository contributes to the overall system while maintaining its own responsibility.

## 9. Architecture References

The detailed functional requirements, data model, API contract, and technical decisions are documented in the original Python and .NET specification directories.

These documents serve as references for understanding the system requirements and adapting the architecture to the target technology stack.