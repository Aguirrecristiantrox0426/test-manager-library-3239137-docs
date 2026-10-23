# Repository Structure – Manager Library

## 1. Introduction

This document describes the organization of the Manager Library project across its six GitHub repositories.

Each repository has a specific responsibility within the overall solution. This separation allows the project documentation, application components, infrastructure, and utilities to be managed independently.

## 2. Repository Overview

The project is organized into six repositories:

| Repository | Main Responsibility |
|---|---|
| `test-manager-library-3239137-docs` | Central project documentation and technical specifications. |
| `test-manager-library-3239137-api` | Backend application and HTTP API. |
| `test-manager-library-3239137-app` | Frontend application. |
| `test-manager-library-3239137-page` | Public presentation website. |
| `test-manager-library-3239137-infra` | Infrastructure and database environment configuration. |
| `test-manager-library-3239137-tool` | Utilities and demonstration data seeding. |

## 3. Repository Responsibilities

### 3.1 Docs Repository

**Repository:** `test-manager-library-3239137-docs`

This repository contains the central technical documentation of Manager Library.

Its responsibilities include:

- Maintaining the project description and scope.
- Documenting functional and non-functional requirements.
- Describing the system architecture.
- Maintaining the data model and API contract references.
- Preserving the original Python and .NET specifications.
- Providing documentation for the other project repositories.

### 3.2 API Repository

**Repository:** `test-manager-library-3239137-api`

This repository is responsible for the backend application developed with PHP and Laravel.

Its responsibilities include:

- Providing HTTP API endpoints.
- Managing authentication and authorization.
- Processing application business rules.
- Managing books, categories, members, loans, and returns.
- Interacting with the PostgreSQL database.
- Providing overdue loan and most borrowed book information.

### 3.3 App Repository

**Repository:** `test-manager-library-3239137-app`

This repository contains the frontend application developed with React.

Its responsibilities include:

- Providing the application user interface.
- Supporting administrative and librarian workflows.
- Displaying information received from the API.
- Sending requests to backend endpoints.
- Presenting information according to the user's permissions.

### 3.4 Page Repository

**Repository:** `test-manager-library-3239137-page`

This repository contains the public presentation website for Manager Library.

Its responsibilities include:

- Presenting general information about the system.
- Communicating the purpose and main features of the project.
- Providing a public-facing entry point for visitors.
- Maintaining the presentation content and visual structure.

### 3.5 Infra Repository

**Repository:** `test-manager-library-3239137-infra`

This repository contains the infrastructure configuration required by the project.

Its responsibilities include:

- Defining the containerized infrastructure environment.
- Configuring the PostgreSQL database service.
- Managing container networking and volumes.
- Documenting the infrastructure configuration.
- Providing the database environment required by the application.

### 3.6 Tool Repository

**Repository:** `test-manager-library-3239137-tool`

This repository contains utilities associated with the project.

Its responsibilities include:

- Providing utility tools for project operations.
- Supporting the preparation of demonstration data.
- Providing data seeding resources.
- Documenting the configuration and use of its utilities.

## 4. Repository Relationships

The repositories work together to support the overall Manager Library solution.

The main relationships are:

- The Docs repository provides the specifications and documentation used as a reference by the other repositories.
- The App repository communicates with the API repository to access application services.
- The API repository processes requests and interacts with the PostgreSQL database configured through the Infra repository.
- The Page repository provides the public presentation of the project.
- The Tool repository provides utilities and demonstration data resources.

## 5. Repository Management

Each repository is maintained independently and has its own version control history.

The project uses Git and GitHub to support:

- Source and documentation version control.
- Branch-based development.
- Pull request reviews.
- Change tracking.
- Collaboration among team members.

## 6. Documentation Consistency

All repositories must maintain consistency with the central project specifications.

Changes to requirements, architecture, data structures, or API contracts must be reflected in the relevant documentation.

The Docs repository serves as the central reference for the overall project.

## 7. Conclusion

The six-repository organization separates the responsibilities of Manager Library into independent but related components.

This structure supports maintainability, documentation consistency, collaboration, and the independent management of each part of the solution.