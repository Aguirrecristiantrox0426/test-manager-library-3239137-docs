# Technology Stack – Manager Library

## 1. Introduction

This document describes the technologies and tools established for the development and operation of Manager Library.

The technology stack is based on the requirements of the technical challenge and the adaptation of the original Python and .NET specifications.

## 2. Core Technologies

| Technology | Version / Specification | Responsibility |
|---|---|---|
| React | As established by the project | Frontend development and user interface. |
| PHP | As required by Laravel | Backend programming language. |
| Laravel | Framework version to be defined | Backend application development and API management. |
| PostgreSQL | 16 | Relational database management. |

## 3. Frontend Technologies

### React

React is the JavaScript library selected to develop the frontend application.

Its responsibilities include:

- Building reusable user interface components.
- Displaying information from the backend.
- Managing user interactions.
- Communicating with the backend through HTTP requests.
- Presenting information according to user permissions.

## 4. Backend Technologies

### PHP

PHP is the programming language selected for the backend application.

It is responsible for processing requests, executing business logic, validating information, and managing communication with the database.

### Laravel

Laravel is the PHP framework selected for backend development.

Its responsibilities include:

- Defining HTTP routes and controllers.
- Organizing application logic.
- Managing request validation.
- Supporting authentication and authorization.
- Coordinating database operations.
- Implementing the documented API contract.

## 5. Database Technology

### PostgreSQL 16

PostgreSQL 16 is the relational database management system selected for Manager Library.

It is responsible for storing and managing:

- System users.
- Book categories.
- Books.
- Library members.
- Loans.
- Loan items.

The database uses the `library` schema and must preserve referential integrity and transaction consistency.

## 6. Communication and Data Exchange

The frontend and backend communicate through an HTTP API.

The system uses:

- HTTP methods to perform operations on resources.
- JSON as the data exchange format.
- JWT for authentication.
- Defined API endpoints for system functionalities.

## 7. Development and Infrastructure Tools

The following tools are associated with the project's repository organization:

| Tool or Component | Responsibility |
|---|---|
| Git | Version control. |
| GitHub | Repository hosting and collaboration. |
| Docker | Containerization and infrastructure configuration, according to the infrastructure repository. |
| PostgreSQL | Database engine. |

Specific versions and configurations not established by the project specifications must be documented when they are formally defined.

## 8. Technology Selection Rationale

The selected technologies support the separation of responsibilities between the frontend, backend, and database.

- React provides a component-based approach for building the user interface.
- PHP with Laravel provides the backend framework for managing application logic and HTTP services.
- PostgreSQL provides relational data storage and transaction management.

This combination represents the target technology stack for the technical challenge.

## 9. Reference Specifications

The original Python and .NET specifications provide the functional and architectural references for the system.

Their technical decisions must be adapted to the target stack:

- Frontend: React.
- Backend: PHP with Laravel.
- Database: PostgreSQL 16.