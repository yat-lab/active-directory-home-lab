# Active Directory Setup

## Domain Information
- Forest Name: yatlab.local
- Domain Name: yatlab.local
- NetBIOS Name: YATLAB
- Domain Controller: DC01

## Active Directory Domain Services (AD DS)
Installed the following role:
- Active Directory Domain Services (AD DS)

The server was promoted to a Domain Controller by:
- Creating a new forest
- Configuring DNS automatically during promotion
- Setting a Directory Services Restore Mode (DSRM) password

## Organizational Units (OUs)
Created the following Organizational Units:
- IT
- HR
- Servers

Purpose of OUs:
- Organize users and computers
- Prepare for future Group Policy Objects (GPOs)
- Simulate department structure in an enterprise environment

## Users
Created the following domain user:
- Thomas Yip
- Gabriel Wong

## Security Groups
Created the following security group:
- IT_Admins
- HR_Users

## Current Environment Structure

yatlab.local
├── IT
│   ├── Thomas Yip
│   └── IT_Admins
├── HR
    ├── Gabriel Wong
│   └── HR_Users
└── Servers

## Goal
This Active Directory environment serves as the foundation of the home lab and will later support:
- Domain-joined client machines
- Group Policy management
- Centralized authentication
- Access control and permission management