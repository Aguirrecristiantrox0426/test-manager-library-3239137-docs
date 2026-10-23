# Project Description – Manager Library

## 1. Introduction

Manager Library is an information system designed to facilitate the administration of small libraries through a digital platform that centralizes the management of books, categories, members, users, and loans.

The system aims to improve the control of bibliographic resources and organize the processes for lending and returning items, enabling administrators and librarians to carry out their tasks in a structured manner.

## 2. Problem Statement

Managing small libraries can be challenging when the recording of books, members, and loans is handled through manual procedures or decentralized tools.

Such situations can lead to data inconsistencies, difficulties in determining the availability of items, and challenges in identifying overdue loans.

Manager Library offers a digital solution that centralizes this information and implements rules to govern the lending and return of items.

## 3. General Objective

To develop an information system for managing the administrative and bibliographic processes of a small library, facilitating the control of books, members, loans, and returns.

## 4. Specific Objectives

- Manage system user information and their respective roles.
- Administer the book catalog and its categories.
- Register and retrieve information regarding library members.
- Manage the lending and return of books.
- Identify overdue loans.
- Generate reports on the most frequently borrowed books.
- Implement authentication and access control mechanisms.

## 5. System Actors

| Actor | Description |
|---|---|
| Administrator | Manages system users and performs administrative functions. |
| Librarian | Administers books, members, loans, and returns. |
| Member | An individual registered with the library who can borrow books. |

**Note:** According to the model described in the specification, members are not required to log in to the platform. ## 6. General Description

Manager Library comprises the following main modules:

- Authentication and user management.
- Category administration.
- Book catalog management.
- Member registration.
- Management of loans and returns.
- Inquiry regarding overdue loans.
- Reports on the most frequently borrowed books.

## 7. Project Technologies

The solution is developed using the technologies established for the challenge:

- **Frontend:** React.
- **Backend:** PHP with Laravel.
- **Database:** PostgreSQL 16.

The original specifications in Python and .NET are retained as reference documents to guide the adaptation of the requirements and architecture to the project's technology stack.