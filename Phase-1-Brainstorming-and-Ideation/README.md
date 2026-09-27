# Brainstorming and Ideation Phase

## Project Name

Script-Controlled ACL – Restrict Record Access Based on Field Value

## Introduction

The Brainstorming and Ideation phase is the first phase of the project.

In this phase, the project idea, problem, objectives, proposed solution, users, and expected benefits are identified.

The project focuses on implementing security and access control in ServiceNow using Access Control Lists (ACLs).

## Problem Statement

In a ServiceNow application, different users may require different levels of access to records.

If all users are given the same access, unauthorized users may be able to view, create, modify, or delete records.

Therefore, a proper access control mechanism is required to restrict users according to their roles and record information.

## Project Idea

The main idea of this project is to implement Script-Controlled Access Control Lists in ServiceNow.

The system controls access to records based on user roles and the value stored in the Branch field.

The project uses the Institution Details table to store student-related information.

## Proposed Solution

The proposed solution is to create a custom table in ServiceNow and apply different ACLs for different operations.

The project implements ACLs for:

- READ
- CREATE
- WRITE
- DELETE

The READ access is controlled using a Branch condition and a script.

The required users are provided with specific roles to control their permissions.

## Main Objective

The main objective of the project is to demonstrate how ServiceNow ACLs can be used to provide controlled and secure access to records.

The project aims to:

- Restrict unauthorized record access.
- Control access using user roles.
- Control record viewing using the Branch field.
- Provide different permissions for different operations.
- Protect important student-related records.
- Demonstrate script-controlled security in ServiceNow.

## User Access Idea

A test user named EEE User is planned for the project.

Different roles are created to control different operations.

The planned roles are:

- bb1 – READ access
- bb2 – CREATE access
- bb3 – WRITE access
- bb4 – DELETE access

The administrator is also considered separately because administrators should retain full access.

## Table Idea

A custom ServiceNow table named Institution Details is planned.

The table is used to store student information.

The planned table fields include:

- Student Roll Number
- Student Name
- Faculty Name
- Branch
- Email
- Phone Number
- Description

## Branch-Based Access Idea

The Branch field is used to create different types of records.

The planned Branch values are:

- EEE
- ECE
- CSE

The Branch field helps demonstrate condition-based access control.

For the READ operation, the project focuses on allowing access to the required EEE records while restricting unauthorized access.

## ACL Idea

The project uses four different ACL operations.

### READ ACL

The READ ACL controls whether a user can view records.

The bb1 role is planned for READ access.

The Branch condition is used to control access to EEE records.

### CREATE ACL

The CREATE ACL controls whether a user can create new records.

The bb2 role is planned for CREATE access.

### WRITE ACL

The WRITE ACL controls whether a user can modify existing records.

The bb3 role is planned for WRITE access.

### DELETE ACL

The DELETE ACL controls whether a user can delete records.

The bb4 role is planned for DELETE access.

## Brainstorming Process

The project idea was developed by identifying the need for secure record access in ServiceNow.

The following points were considered during brainstorming:

1. Identify the need for record-level security.
2. Identify different types of users.
3. Identify the operations that need access control.
4. Create separate roles for different operations.
5. Create a custom table for testing.
6. Add different student-related fields.
7. Add records with different Branch values.
8. Implement ACLs for different operations.
9. Use a script for controlled READ access.
10. Test authorized and unauthorized access.
11. Verify administrator access.
12. Document the final implementation.

## Security Consideration

Security is an important part of the project.

The project is designed to prevent unauthorized users from accessing protected records.

Role-based access control and condition-based access control are considered during the ideation stage.

## Expected Benefits

The proposed project is expected to provide the following benefits:

- Improves record security.
- Restricts unauthorized access.
- Provides role-based permissions.
- Provides condition-based record access.
- Controls different operations separately.
- Helps protect student information.
- Demonstrates ServiceNow ACL functionality.
- Provides practical knowledge of ServiceNow security.
- Helps understand script-controlled access.
- Supports controlled access to application records.

## Expected Outcome

The expected outcome of the project is a ServiceNow application in which access to Institution Details records is controlled using ACLs.

Different roles will be used for different operations.

The READ operation will use the Branch condition and script-based access control.

The project will also verify administrator access and unauthorized access.

## Conclusion

The Brainstorming and Ideation phase defines the basic idea and direction of the project.

The project aims to demonstrate how Script-Controlled ACLs can be used in ServiceNow to protect records and control user permissions.

The identified idea will be developed, tested, documented, and demonstrated in the following project phases.
