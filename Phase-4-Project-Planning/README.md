# Project Planning Phase

## Project Name

Script-Controlled ACL – Restrict Record Access Based on Field Value

## Project Objective

The main objective of this project is to implement script-controlled Access Control Lists (ACLs) in ServiceNow.

The project is planned to restrict access to Institution Details records based on user roles and the Branch field value.

Users belonging to the required role can access the permitted records, while administrators retain full access.

## Project Planning

The project is planned in different stages to implement and verify record-level security in ServiceNow.

The major activities include:

1. Creating the required user.
2. Creating the required roles.
3. Assigning roles to the user.
4. Creating the Institution Details table.
5. Creating the required fields.
6. Creating multiple student records.
7. Creating the READ ACL.
8. Testing the READ access.
9. Creating the CREATE ACL.
10. Testing the CREATE access.
11. Creating the WRITE ACL.
12. Testing the WRITE access.
13. Creating the DELETE ACL.
14. Testing the DELETE access.
15. Verifying the final access control behavior.

## User and Role Planning

A test user named EEE User is created for testing the access control mechanism.

The following roles are planned for the project:

- bb1 – Used for READ access
- bb2 – Used for CREATE access
- bb3 – Used for WRITE access
- bb4 – Used for DELETE access

All required roles are assigned to the EEE User.

## Table Planning

A custom table named Institution Details is planned for storing student information.

Table Name:

u_institution_details

The table contains student-related information such as:

- Student Roll Number
- Student Name
- Faculty Name
- Branch
- Email
- Phone Number
- Description

## Record Planning

Multiple student records are planned with different Branch values.

The Branch values used in the project are:

- EEE
- ECE
- CSE

This allows the ACL to be tested with different record values.

## ACL Planning

Four different ACL operations are planned for the project.

### 1. READ ACL

The READ ACL is planned with:

- Operation: Read
- Role: bb1
- Data Condition: Branch is EEE

The purpose is to control which records can be viewed.

### 2. CREATE ACL

The CREATE ACL is planned with:

- Operation: Create
- Role: bb2

This controls the ability to create new records.

### 3. WRITE ACL

The WRITE ACL is planned with:

- Operation: Write
- Role: bb3

This controls the ability to modify records.

### 4. DELETE ACL

The DELETE ACL is planned with:

- Operation: Delete
- Role: bb4

This controls the ability to delete records.

## Testing Plan

The project is planned to be tested by impersonating users with the required roles.

The following access conditions are verified:

- User with bb1 role can view the permitted EEE branch records.
- User without the required role cannot view the records.
- Admin user can view all records.
- User with bb2 role can create records.
- User with bb3 role can modify records.
- User with bb4 role can delete records.

## Expected Project Outcome

The planned project demonstrates how ServiceNow ACLs can control READ, CREATE, WRITE, and DELETE operations using user roles and record field values.

The project also demonstrates how record-level security can be implemented to prevent unauthorized access.
