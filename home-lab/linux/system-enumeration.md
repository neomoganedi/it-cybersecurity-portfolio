# Linux System Enumeration

## Objective

The objective of this phase was to gather information about the Ubuntu Server system before performing security assessment and hardening.

## System Information

The following information was collected from the Ubuntu Server virtual machine:

- Operating System: Ubuntu Server 26.04 LTS
- Kernel: Linux 7.0.0-29-generic
- Architecture: x86-64
- Virtualization: Oracle VirtualBox
- Hostname: ubuntu-server-lab
- Network Interface: enp0s3
- IP Address: 10.0.2.15/24
- Default Gateway: 10.0.2.2

## Commands Used

The following commands were used during system enumeration:

```bash
hostnamectl
ip addr
ip route
ss -tuln
sudo ufw status verbose
