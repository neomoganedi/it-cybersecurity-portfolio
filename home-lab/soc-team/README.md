# SOC Team Blue-Team Lab

## Overview

This lab demonstrates a practical Security Operations Center (SOC) blue-team workflow using an Ubuntu Server as a monitored security host

The objective was to configure monitoring, collect SSH authentication events, detect suspicious login activity, and implement automated protection using Fail2Ban

## Lab Environment

* **Server:** Ubuntu Server
* **Client:** Windows
* **Network:** Host-only lab network
* **Server IP:** 192.168.56.10
* **Client IP:** 192.168.56.1
* **Service monitored:** SSH
* **Security tool:** Fail2Ban

## Objectives

* Configure and verify SSH access
* Monitor SSH authentication activity
* Generate failed SSH login attempts in a controlled lab
* Review authentication logs
* Configure Fail2Ban to protect SSH
* Verify that suspicious activity is detected
* Verify that the attacking IP address is automatically banned
* Document the investigation and response process

## Security Controls Implemented

### SSH Monitoring

SSH was configured and verified as an active service on the Ubuntu Server.

The server logs SSH authentication events, including:

* Successful authentication
* Invalid users
* Failed authentication attempts
* Connection resets

### Fail2Ban

Fail2Ban was configured with an SSH jail to monitor SSH authentication activity

The configuration was designed to detect repeated failed SSH activity and automatically ban the source IP address

Key configuration values included:

* SSH jail enabled
* SSH port monitored
* Maximum retries configured
* Find time configured
* Ban time configured

## Detection Exercise

From the Windows client, multiple SSH authentication attempts were made using an invalid username

The Ubuntu Server recorded the activity as invalid SSH users originating from:

`192.168.56.1`

The SSH service logs provided evidence of the activity

## Automated Response

Fail2Ban detected the repeated invalid SSH activity

The final Fail2Ban status showed:

* **Total failed:** 3
* **Currently banned:** 1
* **Total banned:** 1
* **Banned IP:** 192.168.56.1

This demonstrated that the security control successfully detected repeated suspicious authentication activity and automatically blocked the source IP

## Investigation Workflow

The lab followed a basic SOC investigation process:

1. Generate suspicious authentication activity
2. Review SSH service logs
3. Identify the source IP address
4. Confirm repeated failed activity
5. Check the Fail2Ban jail status
6. Verify that the source IP was banned
7. Confirm that the security control responded automatically

## Evidence

Screenshots were collected during the lab to demonstrate:

* SSH service status
* SSH authentication events
* Invalid-user activity
* Fail2Ban configuration
* Fail2Ban jail status
* Automatic IP banning

## Skills Demonstrated

* Linux server administration
* SSH security
* Log analysis
* Authentication monitoring
* Incident detection
* Automated incident response
* Fail2Ban configuration
* SOC investigation methodology
* Security documentation

## Key Takeaway

This lab demonstrates a basic blue-team security workflow: **detect - investigate - respond - verify**.

The exercise shows how authentication logs can be used to identify suspicious activity and how an automated security control such as Fail2Ban can respond to repeated SSH attacks

## Lab Status

**Completed**

The core SOC blue-team lab objectives were successfully demonstrated and documented
