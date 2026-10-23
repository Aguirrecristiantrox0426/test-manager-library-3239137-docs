# Project Scope – Manager Library

## 1. Project Overview

Manager Library is an information system designed to support the administrative and operational activities of a small library. The system centralizes information about books, categories, members, users, loans, and returns.

The solution is designed around a web-based architecture using React for the frontend, PHP with Laravel for the backend, and PostgreSQL 16 as the database management system.

## 2. Project Scope

The project includes the design and development specifications for the following functionalities:

### 2.1 User Authentication and Management

- Authenticate administrators and librarians using credentials.
- Manage system users and their roles.
- Provide token-based authentication using JWT.
- Apply role-based access control.

### 2.2 Category Management

- Manage the predefined book categories.
- Associate books with their corresponding categories.

### 2.3 Book Management

- Register new books.
- Consult and list registered books.
- Update book information.
- Manage book availability and copy quantities.
- Apply logical deletion to books instead of permanently removing their records.

### 2.4 Member Management

- Register library members.
- Store and consult member information.
- Associate members with their loan records.

### 2.5 Loan Management

- Register book loans for library members.
- Validate loan conditions before creating a loan.
- Track loan records and their details.
- Control loan due dates.
- Identify overdue loans.

### 2.6 Return Management

- Register the return of individual loan items.
- Update book availability after a return.
- Prevent duplicate returns.
- Preserve loan and return history.

### 2.7 Reports and Queries

- Consult overdue loans.
- Generate reports about the most borrowed books.
- Retrieve relevant information for library administration.

## 3. System Actors

| Actor | Responsibilities |
|---|---|
| Administrator | Manages system users and administrative operations. |
| Librarian | Manages books, members, loans, and returns. |
| Member | Is registered in the library and can request book loans. |

Members are registered in the system but do not authenticate themselves through the application, according to the specification.

## 4. Business Rules

The system must enforce the following business rules:

- Authentication tokens have a validity period of 8 hours.
- Each loan has a maximum duration of 14 days.
- A member can have a maximum of 3 books on loan without returning them.
- Members with overdue loans cannot request additional loans.
- A loan must contain between 1 and 3 loan items.
- The same book cannot be repeated within a single loan.
- Book availability must be updated within the same database transaction used to register the loan.
- Loan items must be returned individually.
- A loan item cannot be returned more than once.
- Loan status is calculated as `open`, `overdue`, or `closed`.

## 5. Project Constraints

The project follows these documented constraints:

- The database management system is PostgreSQL 16.
- The database schema is named `library`.
- Books are subject to logical deletion.
- Loan and return records must be preserved.
- ISBN values must contain 13 digits and be unique among active books.
- Book cover images must use JPG or PNG format and must not exceed 2 MB.
- The system uses role-based access control for administrators and librarians.

## 6. Scope Boundaries

The scope of this document is limited to the functionalities and business rules defined in the official Manager Library specifications.

Features or processes that are not explicitly described in those specifications must not be considered part of the confirmed project scope without further requirements or approval.

## 7. Reference Specifications

The project includes two original specification versions:

- **Python Specification:** Provides requirements and technical design references using Python-oriented decisions.
- **.NET Specification:** Provides requirements and technical design references using .NET-oriented decisions.

Both specifications describe the same business domain. Their requirements and business rules serve as references for adapting the solution to the target technology stack: React, PHP with Laravel, and PostgreSQL 16.