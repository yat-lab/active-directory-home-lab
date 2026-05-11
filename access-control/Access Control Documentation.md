# Access Control Lab

## Overview
This lab demonstrates centralized access control within a Windows domain environment using:
- Group Policy Objects (GPOs)
- NTFS Permissions
- Shared Folder Permissions
- Security Group-based authorization

The environment simulates enterprise-style access management and resource restriction practices.

---

# Group Policy Management (GPO)

## Policy Created
- IT-Restrictions

## Configured Restriction
Enabled:
- Prohibit IT's access to Control Panel and PC settings

---

# Shared Folder Access Control

## Shared Folders Created
- C:\Shares\IT
- C:\Shares\HR

## IT Folder
Allowed:
- IT_Admins → Full Control

Retained:
- SYSTEM
- Administrators
- CREATOR OWNER

Removed:
- Users

## HR Folder
Allowed:
- HR_Users → Full Control

Retained:
- SYSTEM
- Administrators
- CREATOR OWNER

Removed:
- Users


# Skills Practiced
- Group Policy configuration
- Windows access control
- Shared folder administration
- NTFS permission configuration
- Windows file sharing
- Security group-based authorization
- Enterprise Windows administration
