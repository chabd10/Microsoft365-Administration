# Microsoft 365 Administration Lab

Hands-on Microsoft 365 administration lab focused on user management, Exchange Online, Microsoft Entra ID, Intune, and PowerShell administration.

This project demonstrates practical cloud administration and IT support tasks performed in a controlled Microsoft 365 lab environment.

## What This Lab Demonstrates

- Microsoft 365 user administration
- License management
- Exchange Online administration
- Mailbox troubleshooting
- Microsoft Entra ID administration
- Sign-in investigation
- Intune device management
- PowerShell administration
- Cloud-based troubleshooting
- Administrative documentation

## Technologies & Tools

- Microsoft 365 Admin Center
- Microsoft Exchange Online
- Microsoft Entra ID
- Microsoft Intune
- Exchange Online PowerShell
- PowerShell
- Windows 11

## Lab Environment

The lab uses a Microsoft 365 tenant with test users and administrative accounts.

Example test user:

- Anna Schmidt
- Microsoft 365 Business Standard
- Exchange Online mailbox
- Microsoft Entra ID account

All activities are performed in a controlled lab environment for learning and portfolio development.

## Practical Administration Areas

### User & License Management

Tasks include:

- Creating and managing Microsoft 365 users
- Assigning Microsoft 365 licenses
- Reviewing user account information
- Managing cloud identities

### Exchange Online

Tasks include:

- Connecting to Exchange Online using PowerShell
- Reviewing mailbox configuration
- Checking mailbox quotas
- Investigating mailbox capacity issues
- Testing mailbox behavior
- Verifying mailbox functionality

### Microsoft Entra ID

Tasks include:

- Reviewing user identities
- Investigating sign-in activity
- Reviewing authentication failures
- Examining IP and location information
- Reviewing device and browser information
- Investigating suspicious authentication activity

### Microsoft Intune

Tasks include:

- Configuring device management
- Working with automatic enrollment
- Reviewing device management concepts
- Managing Windows devices through Microsoft Intune

### PowerShell Administration

PowerShell was used to perform administrative and troubleshooting tasks across Microsoft 365.

Examples include:

```powershell
Connect-ExchangeOnline
Get-ConnectionInformation
Get-EXOMailbox
Get-MailboxStatistics
```

PowerShell was also used to investigate mailbox configuration and verify administrative changes.

## Troubleshooting Approach

The lab follows an evidence-based troubleshooting process:

```text
Identify the problem
        ↓
Gather evidence
        ↓
Investigate the configuration
        ↓
Identify the likely cause
        ↓
Apply a targeted fix
        ↓
Verify the result
        ↓
Document the outcome
```

The objective is to restore service while making only the changes necessary to resolve the issue.

## Security Investigation

The lab also includes investigation of suspicious Microsoft 365 authentication activity using Microsoft Entra sign-in logs.

The investigation focused on:

- Authentication result
- Error codes
- Source IP
- Approximate location
- Device information
- Browser information
- Authentication method
- Conditional Access information

The investigation demonstrates the importance of distinguishing between failed authentication attempts and confirmed unauthorized access.

## Evidence

Screenshots and supporting documentation are included in the repository to demonstrate practical administration and troubleshooting work.

## Skills Demonstrated

- Microsoft 365 Administration
- Exchange Online
- Microsoft Entra ID
- Microsoft Intune
- PowerShell
- User Administration
- License Management
- Mailbox Administration
- Identity Troubleshooting
- Authentication Investigation
- Cloud Troubleshooting
- Technical Documentation

## Disclaimer

This is a personal hands-on Microsoft 365 administration lab created for learning and portfolio purposes.

Test users, configurations, and security scenarios are performed in a controlled environment and do not represent production systems.
