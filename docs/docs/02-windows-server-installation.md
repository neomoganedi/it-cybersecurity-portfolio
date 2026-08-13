# 02 - Windows Server 2022 Installation

## Objective

Install Windows Server 2022 Standard Evaluation with Desktop Experience inside VirtualBox.

## Installation

The Windows Server 2022 ISO was attached to the DC01 virtual machine.

The following edition was selected:

**Windows Server 2022 Standard Evaluation (Desktop Experience)**

Desktop Experience was selected to provide a graphical interface for administration and troubleshooting.

## Virtual Disk

The virtual machine was configured with:

- 50 GB virtual disk
- VDI format
- Dynamically allocated storage

## Server Configuration

After installation:

- The server was renamed to `DC01`
- A static IPv4 address was configured
- The server was prepared for Active Directory Domain Services

## Evidence

Screenshots documenting the installation process are stored in:

`screenshots/02-server-installation/`

## Status

Installation completed successfully.
