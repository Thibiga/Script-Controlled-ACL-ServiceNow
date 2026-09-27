# Project Development Phase

## Project Name

Script-Controlled ACL – Restrict Record Access Based on Field Value

## Introduction

The development phase involves implementing the planned project in the ServiceNow platform.

The project is developed by creating the required user, roles, custom table, fields, student records, and Access Control Lists (ACLs).

The main purpose is to control access to Institution Details records based on user roles and the Branch field.

## 1. User Creation

A test user named EEE User is created in ServiceNow.

The user details include:

- User ID: EEE User
- First Name: EEE
- Last Name: User
- Email: eeeuser@gmail.com

The user is used for testing the ACL functionality.

## 2. Role Creation

Four custom roles are created for controlling different operations.

The roles are:

- bb1 – READ access
- bb2 – CREATE access
- bb3 – WRITE access
- bb4 – DELETE access

All four roles are assigned to the EEE User.

## 3. Table Creation

A custom table named Institution Details is created in ServiceNow.

Table Name:

u_institution_details

The table is used to store student information.

## 4. Field Creation

The required fields are created in the Institution Details table.

The fields include:

- Student Roll Number
- Student Name
- Faculty Name
- Branch
- Email
- Phone Number
- Description

The Branch field contains the following choices:

- ECE
- EEE
- CSE

## 5. Student Record Creation

Multiple student records are created in the Institution Details table.

Different Branch values are used for the records, including:

- EEE
- ECE
- CSE

These records are used to test the record-level access restrictions.

## 6. READ ACL Development

A READ ACL is created for the Institution Details table.

The READ ACL uses the bb1 role and the Branch field condition.

The data condition is:

Branch is EEE

A script is also added to control access.

Administrators are allowed full access, while the required role is used for the permitted records.

## 7. CREATE ACL Development

A CREATE ACL is created for the Institution Details table.

The ACL requires the bb2 role.

This ACL controls the ability of users to create new records.

## 8. WRITE ACL Development

A WRITE ACL is created for the Institution Details table.

The ACL requires the bb3 role.

This ACL controls the ability of users to modify existing records.

## 9. DELETE ACL Development

A DELETE ACL is created for the Institution Details table.

The ACL requires the bb4 role.

This ACL controls the ability of users to delete records.

## 10. ACL Implementation

The four ACL operations implemented in the project are:

| ACL Operation | Required Role | Purpose |
|---|---|---|
| READ | bb1 | Control record viewing |
| CREATE | bb2 | Control record creation |
| WRITE | bb3 | Control record modification |
| DELETE | bb4 | Control record deletion |

## 11. Development Outcome

The development phase implements role-based and field-based access control in ServiceNow.

The completed implementation provides controlled access to Institution Details records through READ, CREATE, WRITE, and DELETE ACLs.

Administrators retain full access to the records.

## 12. Development Summary

The ServiceNow project has been developed by implementing:

1. User creation
2. Role creation
3. Role assignment
4. Custom table creation
5. Field creation
6. Student record creation
7. READ ACL
8. CREATE ACL
9. WRITE ACL
10. DELETE ACL
