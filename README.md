# Script-Controlled-ACL-ServiceNow
ServiceNow Script-Controlled ACL project
PROJECT OVERALL CONTENT
Project Title

Script-Controlled ACL – Restrict Record Access Based on Field Value

About the Project

This project demonstrates how to implement Script-Controlled Access Control Lists (ACLs) in ServiceNow to restrict users from accessing records unless they meet the required conditions.

The project uses user roles and the Branch field to control access to records in a custom table called Institution Details.

In this project, different roles are used for READ, CREATE, WRITE, and DELETE operations. The READ access also uses the Branch condition. Administrators retain full access to the records.

SERVICE NOW – WHAT WE DID
1. User Creation

First, we created a test user named EEE User in ServiceNow.

The user details were:

User ID: EEE User
First Name: EEE  
Last Name: User
Email: eeeuser@gmail.com

The user was created for testing the ACL access permissions.

2. Role Creation

We created four custom roles:

bb1 – READ access
bb2 – CREATE access
bb3 – WRITE access
bb4 – DELETE access

All four roles were assigned to the EEE User.

3. Table Creation

We created a custom ServiceNow table called:

Institution Details

Table name:

u_institution_details

The table was created to store student-related information.

4. Fields Creation

The table contains the following fields:

Student Roll Number
Student Name
Faculty Name
Branch
Email
Phone Number
Description

The Branch field contains values such as ECE, EEE, and CSE.

5. Student Records

Multiple student records were created with different Branch values such as:

EEE
ECE
CSE

These records were used to test the ACL conditions.

6. ACL Creation

Four ACLs were created:

READ ACL
Role: bb1
Condition: Branch is EEE
CREATE ACL
Role: bb2
WRITE ACL
Role: bb3
DELETE ACL
Role: bb4

The READ ACL uses a script to control access, while the other ACLs control the corresponding operations through their required roles.

7. Testing

The ACLs were tested using different users and operations.

We tested:

READ access
Unauthorized access
Administrator access
CREATE access
WRITE access
DELETE access

The project demonstrates how ACLs can control access to records based on roles and conditions.

PROJECT PHASES
PHASE 1 – BRAINSTORMING AND IDEATION
Project Name

Script-Controlled ACL – Restrict Record Access Based on Field Value

Project Description

This project demonstrates how to implement a script-controlled ACL to restrict users from viewing records unless certain conditions are met.

The main idea is to control access to records based on the user's role and the value stored in the Branch field.

Only users meeting the required access condition can access the permitted records, while administrators retain full access.

Main Idea

The project focuses on:

User access control
Role-based security
Branch-based record access
Script-controlled ACL
READ, CREATE, WRITE, and DELETE operations
PHASE 2 – REQUIREMENT ANALYSIS
Project Requirements

The project requires implementing a Script-Controlled ACL in ServiceNow to control access to records based on the Branch field.

User Requirements

A test user named EEE User is required.

The following roles are required:

bb1
bb2
bb3
bb4

All the required roles are assigned to the test user.

Table Requirements

A custom table named Institution Details is required.

Table name:

u_institution_details

Field Requirements

The table requires:

Student Roll Number
Student Name
Faculty Name
Branch
Email
Phone Number
Description
Record Requirements

Multiple records are required with different Branch values:

EEE
ECE
CSE
ACL Requirements

The project requires four ACL operations:

READ
CREATE
WRITE
DELETE

The READ ACL uses the bb1 role and the Branch is EEE condition.

The CREATE ACL uses bb2.

The WRITE ACL uses bb3.

The DELETE ACL uses bb4.

PHASE 3 – PROJECT DESIGN
Table Design

Table Label: Institution Details

Table Name: u_institution_details

Field Design

The Institution Details table contains:

Student Roll Number
Student Name
Faculty Name
Branch
Email
Phone Number
Description
Branch Design

The Branch field contains:

ECE
EEE
CSE
Role Design

The project uses:

bb1
bb2
bb3
bb4
ACL Design
READ ACL

Role: bb1

Condition: Branch is EEE

CREATE ACL

Role: bb2

WRITE ACL

Role: bb3

DELETE ACL

Role: bb4

The READ ACL also contains the script-controlled access logic.

PHASE 4 – PROJECT PLANNING
Project Objective

The main objective is to implement Script-Controlled ACLs in ServiceNow and control access to records in the Institution Details table.

Planned Activities
Create the EEE User.
Create the required roles.
Assign the roles to the user.
Create the Institution Details table.
Create the required fields.
Create student records.
Create the READ ACL.
Test READ access.
Create the CREATE ACL.
Test CREATE access.
Create the WRITE ACL.
Test WRITE access.
Create the DELETE ACL.
Test DELETE access.
Verify administrator access.
Verify unauthorized access.
Document the project.
Prepare the final demonstration.
Expected Outcome

The planned project demonstrates how ServiceNow ACLs can control READ, CREATE, WRITE, and DELETE operations using roles and record conditions.

PHASE 5 – PROJECT DEVELOPMENT
Development Activities

The project was implemented in the ServiceNow Developer Instance.

1. User Creation

Created:

EEE User

and assigned the required roles.

2. Role Creation

Created:

bb1
bb2
bb3
bb4
3. Table Creation

Created:

Institution Details

Table name:

u_institution_details

4. Field Creation

Created the required student information fields.

5. Record Creation

Created multiple student records using:

EEE
ECE
CSE
6. READ ACL

Created a READ ACL with:

Operation: Read
Role: bb1
Condition: Branch is EEE
Advanced: enabled
Script-controlled access
7. CREATE ACL

Created a CREATE ACL using:

Operation: Create
Role: bb2
8. WRITE ACL

Created a WRITE ACL using:

Operation: Write
Role: bb3
9. DELETE ACL

Created a DELETE ACL using:

Operation: Delete
Role: bb4

These ACL configurations follow the project document's specified operations and roles.

PHASE 6 – PROJECT TESTING
Testing Objective

The purpose of testing is to verify whether the implemented ACLs correctly control access to the Institution Details records.

READ Testing

The READ ACL was tested using the required role and Branch condition.

The access behavior was checked for the EEE User.

Unauthorized Access Testing

A user without the required access was tested.

The system restricted access and displayed a security constraint message.

Administrator Testing

The project was tested using the administrator account.

The administrator was able to access the Institution Details records.

CREATE Testing

The CREATE operation was tested using the required CREATE permission.

WRITE Testing

The WRITE operation was tested by modifying an existing record.

DELETE Testing

The DELETE operation was tested using the required DELETE permission.

Testing Result

The testing demonstrated the access-control behavior of the implemented READ, CREATE, WRITE, and DELETE ACLs.

The project document specifically describes verification using the EEE user, a user without the required role, and the Admin user for READ access.

PHASE 7 – PROJECT DOCUMENTATION
Project Documentation

The complete project implementation and testing details are documented in this phase.

The documentation contains:

Project overview
Project objective
Technologies used
User configuration
Role configuration
Table configuration
Field configuration
Branch values
ACL implementation
READ ACL
CREATE ACL
WRITE ACL
DELETE ACL
Testing summary
Project benefits
Project outcome
Conclusion
Project Outcome

The project demonstrates how ServiceNow ACLs can be used to provide controlled access to records.

It demonstrates:

Role-based access control
Condition-based access control
Record-level security
READ permission
CREATE permission
WRITE permission
DELETE permission
PHASE 8 – PROJECT DEMONSTRATION
Demonstration

A final project demonstration video is prepared to explain the complete implementation.

The demonstration includes:

Project Name
Project Purpose
User and Roles
Institution Details Table
Table Fields
Student Records
READ ACL
CREATE ACL
WRITE ACL
DELETE ACL
READ Testing
Unauthorized Access Testing
Administrator Access Testing
WRITE Testing
DELETE Testing
Project Benefits
Final Output
Conclusion

The demonstration video includes screen sharing and student voice-over/explanation, as required by the faculty instructions.
