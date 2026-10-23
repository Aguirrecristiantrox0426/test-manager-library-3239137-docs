# Non-Functional Requirements – Manager Library

## 1. Introduction

This document defines the non-functional requirements of Manager Library. These requirements establish the quality attributes, technical constraints, and security conditions that the system must satisfy.

## 2. Security Requirements

| ID | Requirement | Description |
|---|---|---|
| NFR-01 | Secure Authentication | The system must authenticate administrators and librarians before granting access to protected resources. |
| NFR-02 | JWT Security | The system must use JWT tokens to manage authenticated sessions. |
| NFR-03 | Token Expiration | Authentication tokens must expire after 8 hours. |
| NFR-04 | Role-Based Access Control | The system must restrict operations according to the user's assigned role. |
| NFR-05 | Protected Resources | The system must prevent unauthorized access to protected endpoints and operations. |

## 3. Data Integrity Requirements

| ID | Requirement | Description |
|---|---|---|
| NFR-06 | Transaction Consistency | Loan registration and book availability updates must be executed within the same database transaction. |
| NFR-07 | Data Preservation | Loan and return records must not be permanently deleted. |
| NFR-08 | Referential Integrity | Relationships between books, categories, members, loans, and users must remain consistent. |
| NFR-09 | ISBN Uniqueness | Active books must have unique ISBN values containing exactly 13 digits. |

## 4. File Management Requirements

| ID | Requirement | Description |
|---|---|---|
| NFR-10 | Supported Image Formats | Book cover images must use JPG or PNG formats. |
| NFR-11 | Maximum Image Size | Book cover images must not exceed 2 MB. |

## 5. Technical Requirements

| ID | Requirement | Description |
|---|---|---|
| NFR-12 | Frontend Technology | The frontend must use React. |
| NFR-13 | Backend Technology | The backend must use PHP with Laravel. |
| NFR-14 | Database Technology | The system must use PostgreSQL 16 as its database management system. |
| NFR-15 | Database Schema | The database must use the `library` schema. |
| NFR-16 | API Communication | The frontend and backend must communicate through the documented HTTP API contract. |

## 6. Maintainability Requirements

| ID | Requirement | Description |
|---|---|---|
| NFR-17 | Modular Organization | The system components must be organized into modules according to their responsibilities. |
| NFR-18 | Documentation Consistency | Technical documentation must remain consistent with the official project specifications. |
| NFR-19 | Technology Adaptation | Technical decisions must reflect the target stack established for the challenge. |

## 7. Operational Constraints

- The system must support the administrative workflows of a small library.
- Protected operations must enforce authentication and authorization.
- Database operations involving related changes must preserve data consistency.
- The system must preserve historical loan and return information.

## 8. Notes

The requirements listed in this document distinguish between explicit technical constraints and quality requirements derived from the documented system rules.

Specific performance targets, availability percentages, backup frequencies, and recovery objectives are not assigned here because they are not established in the available project specifications.