# Windows Server Active Directory Home Lab

## Overview

This project documents the deployment and configuration of a Windows Server 2022 Active Directory Domain Services (AD DS) home lab

The purpose of this lab is to develop practical experience with:

- Windows Server administration
- Active Directory Domain Services
- DNS
- Organizational Units (OUs)
- User and group management
- Group Policy
- Security configuration
- GPO testing and troubleshooting

## Lab Environment

| Component | Configuration |
|---|---|
| Operating System | Windows Server 2022 Standard Evaluation |
| Server Name | DC01 |
| Domain | lab.local |
| Virtualization | VirtualBox |
| IP Address | 192.168.10.10 |
| RAM | 4 GB |
| Disk | ~50 GB |

## Active Directory Configuration

The domain controller was configured with the following Organizational Units:

- Lab-Users
- Lab-Servers
- Lab-Groups
- Lab-Admins

A test user was created and placed in the Lab-Users OU.

A Lab Admin user was also created in the Lab-Admins OU.

## Group Policy

A Group Policy Object named:

`GPO-Lab-Users-Security`

was created and linked to the `Lab-Users` OU.

The GPO was configured with security-related settings as part of the lab.

## GPO Testing

The Group Policy was tested using:

```cmd
gpupdate /force
and
gpresult /r

```text
Lessons Learned

This lab provided practical experience with:

Installing and configuring AD DS
Promoting a Windows Server to a domain controller
Creating and organizing OUs
Creating users and security groups
Linking Group Policy Objects to OUs
Understanding GPO scope and inheritance
Using gpupdate and gpresult for troubleshooting
Investigating authentication issues in an Active Directory environment
