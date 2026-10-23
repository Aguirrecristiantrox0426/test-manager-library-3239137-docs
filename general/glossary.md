# Glossary – Manager Library

## 1. Introduction

This document defines the main technical terms, concepts, and abbreviations used throughout the Manager Library project documentation.

## 2. General Terms

| Term | Definition |
|---|---|
| Manager Library | Information system designed to manage the administrative and bibliographic processes of a small library. |
| Library | Institution or organization responsible for managing and lending bibliographic resources. |
| Member | Registered person who can request books from the library. |
| Administrator | User responsible for managing system users and administrative operations. |
| Librarian | Authorized user responsible for managing books, members, loans, and returns. |
| Book | Bibliographic resource registered in the library catalog. |
| Category | Classification used to organize books according to their subject or type. |
| Loan | Record representing the lending of one or more books to a library member. |
| Loan Item | Individual book associated with a loan record. |
| Return | Process of registering the return of a borrowed book. |
| Overdue Loan | Loan that has passed its due date without all its items being returned. |

## 3. Technical Terms

| Term | Definition |
|---|---|
| API | Application Programming Interface. A mechanism that allows different software components to communicate. |
| REST | Architectural style used to design web services through HTTP methods and resources. |
| HTTP | Hypertext Transfer Protocol, used for communication between clients and servers. |
| JWT | JSON Web Token. A token format used to transmit authentication and authorization information. |
| Frontend | Application component responsible for the user interface and user interaction. |
| Backend | Application component responsible for business logic, data processing, and API services. |
| Database | Organized collection of information stored and managed electronically. |
| PostgreSQL | Relational database management system used to store project information. |
| Laravel | PHP framework used to develop the backend application. |
| React | JavaScript library used to build the frontend user interface. |
| Transaction | Group of database operations treated as a single logical unit. |
| Logical Deletion | Method of marking a record as deleted without physically removing it from the database. |
| Endpoint | Specific API address through which a client accesses a system resource or operation. |
| Authentication | Process of verifying the identity of a user. |
| Authorization | Process of determining which resources or operations an authenticated user can access. |
| Role-Based Access Control (RBAC) | Security model that assigns permissions according to user roles. |
| ISBN | International Standard Book Number, used to identify books. |

## 4. Database Terms

| Term | Definition |
|---|---|
| Entity | Object or concept represented in the database. |
| Primary Key (PK) | Field or combination of fields that uniquely identifies a database record. |
| Foreign Key (FK) | Field that establishes a relationship between database tables. |
| Schema | Logical structure used to organize database objects. |
| Referential Integrity | Principle that ensures relationships between database records remain valid. |

## 5. Abbreviations

| Abbreviation | Meaning |
|---|---|
| API | Application Programming Interface |
| DBMS | Database Management System |
| FR | Functional Requirement |
| HTTP | Hypertext Transfer Protocol |
| ISBN | International Standard Book Number |
| JSON | JavaScript Object Notation |
| JWT | JSON Web Token |
| NFR | Non-Functional Requirement |
| PK | Primary Key |
| REST | Representational State Transfer |
| RBAC | Role-Based Access Control |
| SQL | Structured Query Language |
| UI | User Interface |
| URL | Uniform Resource Locator |

## 6. Loan Status Values

| Status | Definition |
|---|---|
| `open` | Loan that has not yet been fully returned and has not passed its due date. |
| `overdue` | Loan whose due date has passed and still has outstanding items. |
| `closed` | Loan in which all associated items have been returned. |

## 7. Document Usage

This glossary serves as a common reference for all project documentation and helps maintain consistent terminology across the Manager Library repositories.