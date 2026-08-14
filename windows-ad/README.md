# Windows Active Directory Home Lab

## Overview

This project documents a Windows Server Active Directory home lab built to develop practical IT and cybersecurity skills.

The lab focuses on Active Directory Domain Services (AD DS), organizational units, users, security groups, Group Policy, authentication, and basic troubleshooting.

## Lab Environment

- Windows Server
- Active Directory Domain Services (AD DS)
- Domain: `lab.local`
- Domain Controller: `DC01`
- Active Directory Users and Computers
- Group Policy Management

## Active Directory Configuration

A Windows Server was configured as a Domain Controller for the `lab.local` domain.

The following Organizational Units (OUs) were created:

- `Lab-Users`
- `Lab-Servers`
- `Lab-Groups`
- `Lab-Admins`

## Users and Groups

Test accounts and security groups were created to demonstrate basic Active Directory identity management.

A test user was created and added to the appropriate security group.

An administrative account was also created in the `Lab-Admins` OU.

## Group Policy

A Group Policy Object named:

`GPO-Lab-Users-Security`

was created and linked to the `Lab-Users` OU.

The GPO was configured with security-related settings as part of the lab.

## GPO Testing

The Group Policy configuration was tested using:

gpupdate /force

gpresult /r

The testing was used to verify Group Policy processing and investigate policy/application issues

## Authentication Troubleshooting

During testing, an authentication issue was encountered where the test user’s password was rejected

The issue was investigated using Active Directory Users and Computers and Group Policy troubleshooting tools

This demonstrates a realistic troubleshooting scenario involving user authentication and Active Directory configuration

## Lessons Learned

This lab provided practical experience with:

- Installing and configuring AD DS
- Promoting a Windows Server to a domain controller
- Creating and organizing OUs
- Creating users and security groups
- Linking Group Policy Objects to OUs
- Understanding GPO scope and inheritance
- Using `gpupdate` and `gpresult` for troubleshooting
- Investigating authentication issues in an Active Directory environment

## Skills Demonstrated

- Active Directory
- Windows Server Administration
- Identity and Access Management (IAM)
- Group Policy
- User and Group Management
- Authentication Troubleshooting
- Windows Security
