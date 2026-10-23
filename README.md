# Library Manager — System Documentation

## 1. Project Description

**Library Manager** is an information system designed to facilitate the administration and management of small libraries by centralizing the control of books, members, and loans through a digital platform.

The system aims to improve the organization of library processes, reduce errors in data recording, and facilitate the tracking of available items, items currently on loan, and items pending return.

The solution consists of a web-based management application, a public-facing website, a backend service, storage infrastructure, and a tool for generating demonstration data.

## 2. General Objective

To design the technical and functional documentation for a library management system that enables the administration of a book catalog, registration of members, tracking of loans and returns, querying of overdue items, and generation of reports on the most-borrowed books.

## 3. Specific Objectives

- Define the system's functional and non-functional requirements.
- Document the processes for managing books and categories.
- Specify the management of members, loans, and returns.
- Establish the architecture and the responsibilities of each component.
- Define the data model and the relationships between entities.
- Document the services and communication endpoints.
- Establish security and access control criteria.

## 4. System Scope

Library Manager includes the following functionalities:

- Authentication for administrators and librarians.
- Registration and administration of librarians.
- Management of the book catalog.
- Administration of five bibliographic categories.
- Registration and lookup of members.
- Recording of book loans.
- Tracking of returns for individual items.
- Querying of overdue loans.
- Generation of reports on the most-borrowed books.

### Out-of-Scope Functionalities

The system does not include:

- Management of fines or payments.
- Book reservations.
- Loan renewals. - Email or SMS notifications.
- Loans between different branches.
- Bulk data import.

## 5. System Actors

| Actor | Responsibilities |
|---|---|
| Administrator | Manage books, members, librarians, and reports. |
| Librarian | Register loans and returns; look up books, members, and overdue items. |
| Member | An individual who borrows books. Does not have authentication access to the system. |

## 6. Technological Architecture

The solution is organized into the following components:

| Component | Technology | Responsibility |
|---|---|---|
| Server | PHP-Laravel | Request processing, business logic, and API services. |
| Interface | React | Management interface for administrators and librarians. |
| Database | PostgreSQL 16 | Storage for users, books, members, and loans. |
| Public Site | HTML, CSS, and JavaScript | Presentation and general system information. |
| Infrastructure | Docker | Organization of services and execution environments. |
| Tools | JavaScript/Node.js | Generation of demonstration data via the API. |

## 7. Repository Organization

The project is divided into six repositories, each with a specific responsibility.

| Repository | Description |
|---|---|
| [DOCS](https://github.com/Aguirrecristiantrox0426/test-manager-library-3239137-docs) | Functional, technical, and architectural documentation of the system. |
| [API](https://github.com/Aguirrecristiantrox0426/test-manager-library-3239137-api) | Documentation for the backend and its REST services, developed using Laravel. |
| [APPLICATION](https://github.com/Aguirrecristiantrox0426/test-manager-library-3239137-app) | Documentation for the web application developed using React. |
| [PAGE](https://github.com/Aguirrecristiantrox0426/test-manager-library-3239137-page) | Documentation for the public presentation site. |
| [INFRA](https://github.com/Aguirrecristiantrox0426/test-manager-library-3239137-infra) | Documentation for infrastructure, containers, and the database. |
| [TOOL](https://github.com/Aguirrecristiantrox0426/test-manager-library-3239137-tool) | Documentation for tools used to generate demonstration data. |

## 8. System Documentation

This repository centralizes the specifications and documents that guide the definition of the system.

### General Documentation

- Project description.
- Scope and objectives.
- Functional requirements.
- Non-functional requirements.
- Glossary of terms.

### Architectural Documentation

- General architecture.
- Technologies used.
- Repository organization.
- Component responsibilities.

### Technical Specifications

Two reference versions of the system are maintained:

- **spec-.net:** reference specification oriented toward .NET.
- **sp