# PHASE 2 – REQUIREMENT ANALYSIS

## Project Title

**Script-Controlled ACL – Restrict Record Access Based on Field Value**

## 1. Introduction

Requirement Analysis is the process of identifying the requirements needed to develop and implement the proposed ServiceNow project.

The project focuses on implementing Script-Controlled Access Control Lists (ACLs) in ServiceNow. The main requirement is to restrict access to records based on the value of the Branch field. In this project, users belonging to the EEE branch should be allowed to access EEE-related records, while administrators should retain full access.

The project uses ServiceNow users, roles, a custom table, records, and ACL rules to control access.

## 2. Existing System

In a basic record management system, users may have access to records without sufficient field-based restrictions.

If appropriate access controls are not configured, users may be able to view or modify records that they are not supposed to access.

Therefore, a controlled record-level security mechanism is required.

## 3. Problem in Existing System

The main problems identified are:

* Unauthorized users may access records.
* Record access may not be restricted based on specific field values.
* Different operations such as Read, Create, Write, and Delete require separate access control.
* Sensitive student information requires proper security.
* Administrators need complete access while normal users require restricted access.

## 4. Proposed System

The proposed system uses ServiceNow Script-Controlled ACLs to manage access to records.

A custom table named **Institution Details** is created to store student-related information.

The Branch field contains the values:

* ECE
* EEE
* CSE

ACLs are then configured to control Read, Create, Write, and Delete operations.

The READ ACL uses a script and role-based conditions to control record visibility. Administrators are allowed full access, while the required user role is used for EEE-related access.

The project document specifies separate ACLs for Create, Write, and Delete operations using roles `bb2`, `bb3`, and `bb4`.

## 5. Functional Requirements

The system shall provide the following functions:

### 5.1 User Creation

The system should allow creation of the required EEE user.

### 5.2 Role Creation

The system should allow creation of roles:

* bb1
* bb2
* bb3
* bb4

These roles are assigned to the EEE User as required.

### 5.3 Table Creation

The system should provide a custom table named:

**Institution Details**

Table name:

`u_institution_details`

### 5.4 Field Management

The table should contain fields for:

* Student Roll Number
* Student Name
* Faculty Name
* Branch
* Email
* Phone Number
* Description

The Branch field should provide ECE, EEE, and CSE choices.

### 5.5 Record Creation

The system should allow creation of multiple student records with different branch values such as ECE, EEE, and CSE.

### 5.6 Read Access Control

The system should restrict record visibility according to the configured ACL and branch-related requirement.

### 5.7 Create Access Control

A CREATE ACL should control who can create new records using the `bb2` role.

### 5.8 Write Access Control

A WRITE ACL should control who can modify records using the `bb3` role.

### 5.9 Delete Access Control

A DELETE ACL should control who can delete records using the `bb4` role.

### 5.10 Administrator Access

Administrators should retain full access to the records.

## 6. Non-Functional Requirements

The project should satisfy the following requirements:

### Security

The system should prevent unauthorized access to protected records.

### Reliability

The configured ACLs should consistently apply the defined access rules.

### Maintainability

Roles and ACL configurations should be organized so that they can be managed easily.

### Usability

Authorized users should be able to access the records and operations permitted to them.

### Performance

The access control mechanism should operate within the ServiceNow platform without unnecessarily affecting normal record access.

## 7. User Requirements

The project involves the following types of users:

### Administrator

* Has full access to the records.
* Can configure users, roles, tables, and ACLs.
* Can verify the access-control behavior.

### EEE User

* Uses the assigned roles.
* Access to records is controlled through the configured ACLs.
* Can perform operations according to the roles assigned.

### Unauthorized User

* Should not receive access to protected records when the required access conditions are not satisfied.

## 8. Hardware Requirements

The project requires:

* Computer or laptop
* Keyboard
* Mouse
* Internet connection

## 9. Software Requirements

The project requires:

* ServiceNow platform
* Web browser
* ServiceNow user account
* ServiceNow administrative access

## 10. Data Requirements

The system requires student-related information including:

* Student Roll Number
* Student Name
* Faculty Name
* Branch
* Email
* Phone Number
* Description

The Branch field is important for the access-control requirement because the project uses branch-related access restrictions.

## 11. Security Requirements

The system should:

* Restrict unauthorized record access.
* Use roles to control operations.
* Use ACLs for Read, Create, Write, and Delete operations.
* Provide administrators with full access.
* Apply the defined access conditions consistently.

The project specifically demonstrates record-level security using Script-Controlled ACLs.

## 12. Input Requirements

The following inputs are required:

* User details
* Role details
* Student details
* Branch value
* ACL configuration
* Required roles for different operations

## 13. Output Requirements

The expected outputs are:

* Authorized users can access permitted records.
* Unauthorized users are restricted.
* Administrators can access all required records.
* Create, Write, and Delete operations are controlled according to assigned roles.
* The system demonstrates successful record-level security.

## 14. Project Constraints

The project depends on:

* Availability of a ServiceNow environment.
* Appropriate administrative permissions.
* Correct role configuration.
* Correct ACL configuration.
* Proper creation of users, records, and table fields.

Incorrect role or ACL configuration may affect the expected access behavior.

## 15. Requirement Summary

The project requires a ServiceNow environment with a custom Institution Details table, required student-related fields, users, roles, records, and Script-Controlled ACLs.

The major requirement is to control access to records based on the configured security rules. Separate ACLs are required for Read, Create, Write, and Delete operations.

The final system should demonstrate controlled access for users while allowing administrators to retain full access.
