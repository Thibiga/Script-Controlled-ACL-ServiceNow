# PHASE 3 – PROJECT DESIGN

## Project Title

**Script-Controlled ACL – Restrict Record Access Based on Field Value**

## 1. Introduction

Project Design defines the technical structure and workflow of the proposed ServiceNow application.

The project is designed to demonstrate how Script-Controlled Access Control Lists can be used to restrict access to records according to user roles and field values.

The system uses a custom table called **Institution Details** to store student-related information. Access to the records is controlled through ACL rules for Read, Create, Write, and Delete operations.

## 2. Design Objective

The main objective of the project design is to create a secure record-management structure where:

* Users are assigned appropriate roles.
* Student information is stored in a custom table.
* Branch information is maintained using a Choice field.
* Access is controlled using ACLs.
* Different roles control different operations.
* Administrators retain full access.
* Unauthorized users are restricted.

## 3. High-Level System Architecture

The proposed system consists of the following major components:

**User → Roles → ServiceNow ACL → Institution Details Table → Student Records**

The user first authenticates into the ServiceNow environment. Based on the user's assigned roles and the configured ACL rules, the system determines whether the requested operation is permitted.

## 4. User Design

The project requires an EEE user.

User details include:

* User ID: EEE User
* First Name: EEE
* Last Name: User
* Email: [eeeuser@gmail.com](mailto:eeeuser@gmail.com)

The user is assigned the required roles for testing access control.

## 5. Role Design

Four custom roles are designed:

| Role | Purpose                    |
| ---- | -------------------------- |
| bb1  | Required for Read access   |
| bb2  | Required for Create access |
| bb3  | Required for Write access  |
| bb4  | Required for Delete access |

These roles are assigned to the EEE User as specified in the project procedure.

## 6. Table Design

A custom table is designed for storing student information.

**Table Label:** Institution Details

**Table Name:** `u_institution_details`

The table is designed as a standalone table and contains fields related to student and faculty information.

## 7. Field Design

The Institution Details table contains the following fields:

| Field               | Type             |
| ------------------- | ---------------- |
| Student Roll Number | Auto Number      |
| Student Name        | Reference – User |
| Faculty Name        | Reference – User |
| Branch              | Choice           |
| Email               | String           |
| Phone Number        | String           |
| Description         | Multi String     |

The Branch field contains the choices:

* ECE
* EEE
* CSE

## 8. Record Design

Multiple student records are created in the table.

The records contain different branch values such as:

* ECE
* EEE
* CSE

This variation is important for testing the branch-based access requirement.

## 9. ACL Design

The project contains four major ACL operations:

### READ ACL

Controls whether a user can view records.

### CREATE ACL

Controls whether a user can create new records.

### WRITE ACL

Controls whether a user can modify existing records.

### DELETE ACL

Controls whether a user can delete records.

## 10. READ ACL Design

The READ ACL is designed with:

* Type: Record
* Operation: Read
* Name: `u_institution_details`
* Active: Enabled
* Advanced: Enabled
* Required Role: `bb1`
* Data condition: Branch is EEE

The script also provides full access to administrators and controls access for other users.

## 11. CREATE ACL Design

The CREATE ACL is configured for:

* Type: Record
* Operation: Create
* Name: `u_institution_details`
* Active: Enabled
* Required Role: `bb2`

This controls who can create new Institution Details records.

## 12. WRITE ACL Design

The WRITE ACL is configured for:

* Type: Record
* Operation: Write
* Name: `u_institution_details`
* Active: Enabled
* Required Role: `bb3`

This controls who can modify records.

## 13. DELETE ACL Design

The DELETE ACL is configured for:

* Type: Record
* Operation: Delete
* Name: `u_institution_details`
* Active: Enabled
* Required Role: `bb4`

This controls who can delete records.

## 14. System Workflow

The designed workflow is:

1. Create the required user.
2. Create custom roles.
3. Assign roles to the user.
4. Create the Institution Details table.
5. Create required fields.
6. Create student records.
7. Configure READ ACL.
8. Configure CREATE ACL.
9. Configure WRITE ACL.
10. Configure DELETE ACL.
11. Test the system using different users.
12. Verify the access-control behavior.

## 15. Security Design

The security design is based on:

* User roles
* ACL operations
* Branch field values
* Server-side script logic
* Administrator privileges

This design ensures that record access is controlled rather than allowing unrestricted access.

## 16. Expected Design Behavior

The expected behavior is:

* EEE-related access is controlled using the configured READ ACL.
* Users without the required role are restricted.
* Users with required roles receive the corresponding operation access.
* Administrators retain full access.
* Create, Write, and Delete operations are controlled separately.

## 17. Conclusion

The project design provides a structured security model for the Institution Details table. By combining roles, field values, and ACL rules, the design provides controlled access to student records.

The design also provides a clear separation between Read, Create, Write, and Delete permissions.
