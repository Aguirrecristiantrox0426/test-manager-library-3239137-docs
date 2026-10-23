# Functional Requirements – Manager Library

## 1. Introduction

This document describes the functional requirements of Manager Library. These requirements define the operations and services that the system must provide to administrators, librarians, and library members.

## 2. User Authentication and Management

| ID | Requirement | Description |
|---|---|---|
| FR-01 | User Authentication | The system must allow administrators and librarians to authenticate using their credentials. |
| FR-02 | JWT Authentication | The system must generate authentication tokens using JWT after successful authentication. |
| FR-03 | Token Validation | The system must validate authentication tokens before allowing access to protected resources. |
| FR-04 | User Management | The administrator must be able to manage system users. |
| FR-05 | Role Assignment | The system must assign roles to users according to their responsibilities. |
| FR-06 | Access Control | The system must restrict access to functionalities according to the authenticated user's role. |

## 3. Category Management

| ID | Requirement | Description |
|---|---|---|
| FR-07 | Category Listing | The system must allow users with the appropriate permissions to consult the predefined book categories. |
| FR-08 | Category Association | The system must allow books to be associated with their corresponding categories. |

## 4. Book Management

| ID | Requirement | Description |
|---|---|---|
| FR-09 | Book Registration | The system must allow authorized users to register books. |
| FR-10 | Book Consultation | The system must allow authorized users to list and consult registered books. |
| FR-11 | Book Update | The system must allow authorized users to update book information. |
| FR-12 | Book Deactivation | The system must support logical deletion of books without permanently removing their records. |
| FR-13 | ISBN Validation | The system must validate that ISBN values contain 13 digits and are unique among active books. |
| FR-14 | Book Cover Management | The system must accept JPG and PNG book cover images with a maximum file size of 2 MB. |

## 5. Member Management

| ID | Requirement | Description |
|---|---|---|
| FR-15 | Member Registration | The system must allow authorized users to register library members. |
| FR-16 | Member Consultation | The system must allow authorized users to consult registered member information. |
| FR-17 | Member Loan History | The system must maintain the relationship between members and their loan records. |

## 6. Loan Management

| ID | Requirement | Description |
|---|---|---|
| FR-18 | Loan Registration | The system must allow authorized users to register loans for library members. |
| FR-19 | Loan Item Validation | The system must validate that each loan contains between 1 and 3 items and does not repeat the same book. |
| FR-20 | Loan Eligibility Validation | The system must prevent members with overdue loans from requesting additional loans. |
| FR-21 | Maximum Loan Limit | The system must prevent a member from having more than 3 books on loan without returning them. |
| FR-22 | Loan Due Date | The system must establish a loan period of 14 days. |
| FR-23 | Book Availability Update | The system must update book availability within the same database transaction used to register the loan. |
| FR-24 | Loan Status Calculation | The system must calculate the loan status as `open`, `overdue`, or `closed`, according to its dates and return status. |
| FR-25 | Loan History | The system must preserve loan records and their associated items. |

## 7. Return Management

| ID | Requirement | Description |
|---|---|---|
| FR-26 | Individual Item Return | The system must allow each loan item to be returned individually. |
| FR-27 | Duplicate Return Prevention | The system must prevent a loan item from being returned more than once. |
| FR-28 | Book Availability Restoration | The system must update book availability after a successful return. |
| FR-29 | Return History | The system must preserve return information and its relationship with the corresponding loan item. |

## 8. Overdue Loans and Reports

| ID | Requirement | Description |
|---|---|---|
| FR-30 | Overdue Loan Consultation | The system must provide a way to consult overdue loans. |
| FR-31 | Most Borrowed Books Report | The system must generate a report identifying the most borrowed books. |

## 9. Health Check

| ID | Requirement | Description |
|---|---|---|
| FR-32 | System Health Endpoint | The system must provide a health check endpoint to verify whether the application is responding. |

## 10. General Considerations

- All protected operations must validate authentication and authorization.
- Business rules must be enforced before registering loans and returns.
- Loan and return records must remain available for historical consultation.
- Functional requirements must remain consistent with the official Python and .NET specifications and their adaptation to the target technology stack.