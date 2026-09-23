# Project Design Phase

## Table Design

Table Label: Institution Details

Table Name: u_institution_details

## Field Design

Student Roll Number – Auto Number
Student Name – Reference User
Faculty Name – Reference User
Branch – Choice (ECE, EEE, CSE)
Email – String
Phone Number – String
Description – Multi String

## Role Design

bb1
bb2
bb3
bb4

## ACL Design

READ ACL – Role: bb1 – Data condition: Branch is EEE

CREATE ACL – Role: bb2

WRITE ACL – Role: bb3

DELETE ACL – Role: bb4

Administrators retain full access.
