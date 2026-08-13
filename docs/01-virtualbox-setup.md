# 01 - VirtualBox Lab Setup

## Objective

Create a virtualized Windows Server 2022 environment to serve as the foundation for an Active Directory home lab.

## Host Hardware

| Component | Specification |
|---|---|
| Operating System | Windows 11 |
| RAM | 8 GB |
| Storage | 191 GB |
| Processor | 12th Gen Intel Core i5-1235U |

## Virtual Machine

| Setting | Configuration |
|---|---|
| VM Name | DC01 |
| Operating System | Windows Server 2022 |
| RAM | 4096 MB |
| CPU | 2 |
| Disk | 50 GB |
| Network Adapter | NAT |
| Pointing Device | USB Tablet |
| Graphics Controller | VBoxSVGA |

## Purpose

DC01 is the first virtual machine in the home lab and will provide:

- Active Directory Domain Services
- DNS
- Domain authentication
- Group Policy
- User and group management

## Lab Network

The domain controller uses the following static configuration:

| Setting | Value |
|---|---|
| Hostname | DC01 |
| IP Address | 192.168.10.10 |
| Subnet Mask | 255.255.255.0 |
| Domain | lab.local |

## Status

-  Virtual machine created
-  Windows Server 2022 installed
-  Static IP configured
-  Server renamed to DC01
-  Active Directory Domain Services installed
-  DC01 promoted to domain controller
-  DNS installed
-  Active Directory structure created
-  Group Policy created
