# Project Documentation Phase

## Project Name

Script-Controlled ACL – Restrict Record Access Based on Field Value

## Project Overview

This project demonstrates the implementation of Script-Controlled Access Control Lists (ACLs) in ServiceNow.

The project is designed to control access to records in the Institution Details table based on user roles and the Branch field.

The project uses different roles to control READ, CREATE, WRITE, and DELETE operations.

## Project Objective

The main objective of this project is to implement record-level access control in ServiceNow.

The project restricts access to Institution Details records based on the required roles and Branch condition.

Administrators retain full access to the records.

## Technologies Used

- ServiceNow
- ServiceNow Developer Instance
- Access Control Lists (ACLs)
- ServiceNow Scripting
- Role-Based Access Control

## User Configuration

A test user named EEE User is created in ServiceNow.

The following roles are assigned to the user:

- bb1
- bb2
- bb3
- bb4

These roles are used to test different access operations.

## Table Configuration

A custom table named Institution Details is created.

Table Name:

u_institution_details

The table stores student-related information.

## Fields Used

The Institution Details table contains the following fields:

- Student Roll Number
- Student Name
- Faculty Name
- Branch
- Email
- Phone Number
- Description

## Branch Values

The Branch field contains different values used for testing:

- EEE
- ECE
- CSE

These values are used to verify the record access condition.

## ACL Implementation

Four ACL operations are implemented in the project.

### READ ACL

Role:

bb1

Condition:

Branch is EEE

The READ ACL controls the viewing of records.

### CREATE ACL

Role:

bb2

The CREATE ACL controls the creation of new records.

### WRITE ACL

Role:

bb3

The WRITE ACL controls modification of existing records.

### DELETE ACL

Role:

bb4

The DELETE ACL controls deletion of records.

## Script-Controlled Access

The READ ACL uses a script to control record access.

Administrators are allowed full access.

The required role is used to provide access to the permitted records.

Other users are restricted from accessing the records.

## Testing Summary

The implemented ACLs are tested to verify their functionality.

The following operations are tested:

- READ access
- CREATE access
- WRITE access
- DELETE access
- Administrator access
- Unauthorized access

The testing confirms the intended access control behavior of the project.

## Project Outcome

The project demonstrates how ServiceNow ACLs can be used to control access to records.

The project provides an example of role-based and condition-based access control.

It also demonstrates how different permissions can be applied to different operations such as READ, CREATE, WRITE, and DELETE.

## Project Benefits

- Provides controlled access to records.
- Helps prevent unauthorized access.
- Demonstrates role-based access control.
- Demonstrates condition-based record access.
- Provides separate permissions for different operations.
- Helps understand ServiceNow ACL implementation.
- Improves record-level security.

## Conclusion

The Script-Controlled ACL project successfully demonstrates access control in ServiceNow.

Different roles are used to control READ, CREATE, WRITE, and DELETE operations.

The project also demonstrates how record access can be restricted using the Branch field and how administrators can retain full access.

The completed implementation and testing provide a practical understanding of ACL-based security in ServiceNow.
