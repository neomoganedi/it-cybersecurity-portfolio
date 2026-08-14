# Security Controls & Hardening

## Overview

This document describes the security controls implemented and tested during the Windows Active Directory home lab.

The objective was to gain practical experience with identity management, access control, Group Policy, authentication, and basic Windows Server security

## Active Directory Security

Active Directory Domain Services (AD DS) was configured to provide centralized identity and access management for the `lab.local` domain

The environment included separate Organizational Units (OUs) for users, servers, groups, and administrators

This structure provides a foundation for applying security controls to specific groups of objects

## User and Group Management

Dedicated user accounts and security groups were created rather than relying on a single administrative account for all activities

The lab included:

- Test User
- Lab Admin
- Lab-Users
- Lab-Admins
- Lab-Groups
- Lab-Servers

Separating users and administrators supports the principle of least privilege and makes it easier to apply appropriate security policies

## Group Policy

A security-focused Group Policy Object named:

`GPO-Lab-Users-Security`

was created and linked to the `Lab-Users` OU.

Group Policy provides centralized control over security settings and user or computer configuration within the domain

## Authentication Security

Authentication testing was performed using the Test User account

An authentication issue was encountered when the Test User's password was rejected

The issue was investigated as part of the troubleshooting process

This demonstrated the importance of verifying user account configuration, credentials, Group Policy processing, and Active Directory configuration when investigating authentication failures

## Group Policy Verification

Group Policy processing was investigated using:

gpupdate /force
gpresult /r

The gpresult /r output was also used to investigate why certain Group Policy settings were not being applied as expected

## Least Privilege

The lab demonstrated the importance of separating standard user accounts from administrative accounts

Administrative access should be limited to accounts that require it, while normal user accounts should operate with the minimum permissions necessary

This reduces the potential impact of compromised credentials

This lab provided practical experience with several foundational Active Directory security concepts

The environment demonstrated how Organizational Units, users, groups, Group Policy, authentication controls, and troubleshooting can be combined to create a more structured and manageable Windows security environment

The lab also identified areas for future improvement, particularly around authentication troubleshooting, password policies, auditing, and additional Group Policy security controls
