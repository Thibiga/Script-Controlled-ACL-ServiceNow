# Project Testing Phase

## Testing Objective

The objective of this phase is to verify whether the Script-Controlled ACLs work correctly in ServiceNow.

## READ ACL Testing

The READ ACL is tested using the EEE User.

The user with the required bb1 role is tested to verify access to the permitted EEE branch records.

Users without the required access are also tested to verify that unauthorized records cannot be accessed.

## CREATE ACL Testing

The CREATE ACL is tested using the required bb2 role.

The user is verified to ensure that a new Institution Details record can be created.

## WRITE ACL Testing

The WRITE ACL is tested using the required bb3 role.

The user is verified to ensure that permitted records can be modified.

## DELETE ACL Testing

The DELETE ACL is tested using the required bb4 role.

The user is verified to ensure that permitted records can be deleted.

## Administrator Testing

The administrator account is tested to verify that administrators retain full access to the records.

## Expected Result

The ACLs should correctly control READ, CREATE, WRITE, and DELETE operations according to the assigned roles and conditions.
