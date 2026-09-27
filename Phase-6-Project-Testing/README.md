# Project Testing Phase

## Project Name

Script-Controlled ACL – Restrict Record Access Based on Field Value

## Testing Objective

The main objective of this testing phase is to verify whether the Access Control Lists (ACLs) implemented in ServiceNow are working correctly.

The project contains different ACLs for READ, CREATE, WRITE, and DELETE operations.

Each ACL is tested with the required user roles to verify that authorized users can perform the permitted operations and unauthorized users are restricted.

The testing also verifies that administrators retain full access to the Institution Details records.

## Testing Environment

The testing is performed in the ServiceNow Developer Instance.

The custom table used for testing is:

Institution Details

Table Name:

u_institution_details

The test user created for the project is:

EEE User

The roles used for testing are:

- bb1 – READ access
- bb2 – CREATE access
- bb3 – WRITE access
- bb4 – DELETE access

## Test Data

Multiple Institution Details records are created with different Branch values.

The Branch values used for testing are:

- EEE
- ECE
- CSE

Different branch values are used to verify whether the READ ACL correctly controls record access based on the Branch condition.

## READ ACL Testing

The READ ACL is tested first to verify record viewing permissions.

The READ ACL uses the bb1 role and the Branch condition.

The user with the required bb1 role is tested to verify whether the permitted EEE branch records can be viewed.

Users without the required access are also tested to verify that access to the records is restricted.

The administrator account is tested separately to verify that the administrator can view all records.

### Expected Result

- User with the required bb1 role can access the permitted EEE records.
- Unauthorized users cannot access the records.
- Administrator can access all records.

## CREATE ACL Testing

The CREATE ACL is tested to verify whether a user with the bb2 role can create a new Institution Details record.

The New button and record creation functionality are checked for the authorized user.

The purpose of this test is to confirm that the CREATE ACL allows record creation only for users with the required role.

### Expected Result

The user with the required bb2 role should be able to create a new Institution Details record.

Users without the required CREATE permission should not be allowed to create records.

## WRITE ACL Testing

The WRITE ACL is tested to verify whether a user with the bb3 role can modify an existing Institution Details record.

An existing permitted record is opened and the available fields are checked for modification.

The user attempts to update the record and save the changes.

### Expected Result

The user with the required bb3 role should be able to modify the permitted record.

Users without the required WRITE permission should not be allowed to modify the record.

## DELETE ACL Testing

The DELETE ACL is tested to verify whether a user with the bb4 role can delete an Institution Details record.

A test record is selected and the delete operation is checked.

The purpose of this test is to confirm that the DELETE ACL controls record deletion based on the assigned role.

### Expected Result

The user with the required bb4 role should be able to delete the permitted record.

Users without the required DELETE permission should not be allowed to delete records.

## Administrator Access Testing

The administrator account is also tested during the project.

The administrator is verified to ensure that full access is available for the Institution Details table.

The administrator should be able to view and manage the records without the restrictions applied to normal users.

### Expected Result

The administrator should retain full access to the Institution Details records.

## ACL Testing Summary

The following ACL operations are tested:

1. READ – Tested using the bb1 role.
2. CREATE – Tested using the bb2 role.
3. WRITE – Tested using the bb3 role.
4. DELETE – Tested using the bb4 role.

The tests are performed to verify that each ACL provides the expected access according to the assigned role.

## Test Result

The testing confirms the working of the Script-Controlled ACL implementation.

The READ ACL controls record viewing based on the required role and Branch condition.

The CREATE ACL controls the creation of new records.

The WRITE ACL controls modification of existing records.

The DELETE ACL controls deletion of records.

Administrator access is also verified.

## Final Testing Outcome

The project successfully demonstrates role-based and condition-based access control in ServiceNow.

The implemented ACLs provide controlled access to the Institution Details table.

The testing phase verifies the intended behavior of the READ, CREATE, WRITE, and DELETE operations.

The results demonstrate how ServiceNow ACLs can be used to protect records and restrict unauthorized access.
