# Troubleshooting

## Overview

Troubleshooting was performed during the Windows Active Directory lab to investigate Group Policy processing and user authentication issues.

The purpose of the troubleshooting process was to identify configuration problems, verify system behaviour, and document the results.

## Issue 1 — Test User Authentication Failure

### Problem

During authentication testing, the Test User account was unable to authenticate because the password was rejected.

### Investigation

The following areas were reviewed:

- Test User account in Active Directory Users and Computers
- User account placement within the appropriate OU
- Security group membership
- Domain configuration
- Group Policy processing
- User credentials

### Result

The authentication issue was resolved by resetting the 'Test User' password

## Issue 2 — Group Policy Testing

### Problem

The Group Policy configuration needed to be verified after creating and linking the security-focused GPO

### Commands Used

- gpupdate /force

Investigation

The gpresult /r output was reviewed to determine:

Which security groups were associated with the logged-in account
Whether Group Policy information was being processed
Whether policies were being filtered
Whether additional troubleshooting was required

he output provided useful information about Group Policy processing and showed that some policy information was being filtered

## Active Directory Object Creation

During the lab, an issue was encountered while attempting to create an Active Directory object
The error indicated that Windows could not create the requested object
The issue was treated as a troubleshooting observation rather than modifying the environment without understanding the cause

## Lessons From Troubleshooting

Verify account configuration before changing settings.
Confirm Group Policy processing rather than assuming a policy was applied
Use built-in Windows tools to gather evidence.
Document unexpected behaviour
Avoid making undocumented changes simply to make a test appear successful
Distinguish between a confirmed result and an unresolved issue

Future Troubleshooting

## Future testing should include:

Resetting the Test User password
Verifying account status and lockout state
Testing authentication from a domain-joined Windows client
Reviewing relevant Windows security event logs
Verifying DNS and domain connectivity
Reviewing GPO security filtering and inheritance
Testing the GPO against a standard domain user
