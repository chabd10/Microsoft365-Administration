# Exchange Online Administration

This lab demonstrates practical Exchange Online administration and troubleshooting using Microsoft 365 and Exchange Online PowerShell.

The objective is to investigate mailbox configuration, identify mailbox capacity issues, apply controlled administrative changes, and verify that mailbox functionality is restored.

## Exchange Online PowerShell

Exchange Online PowerShell was used to connect to the Microsoft 365 tenant and perform mailbox administration tasks.

Example connection:

```powershell
Connect-ExchangeOnline -UserPrincipalName <admin-account> -DisableWAM
```

The connection was verified using:

```powershell
Get-ConnectionInformation
```

A successful connection allows Exchange Online administration to be performed through PowerShell.

## Mailbox Administration

Mailbox information was investigated using Exchange Online PowerShell.

Example:

```powershell
Get-EXOMailbox -Identity <user> |
    Select DisplayName,PrimarySmtpAddress,RecipientTypeDetails
```

Mailbox quota information was reviewed using:

```powershell
Get-EXOMailbox -Identity <user> -PropertySets Quota |
    Select DisplayName,IssueWarningQuota,ProhibitSendQuota,ProhibitSendReceiveQuota
```

These checks help determine the mailbox configuration and whether capacity limits may be contributing to a reported issue.

## Mailbox Capacity Troubleshooting

A controlled mailbox-capacity scenario was created to reproduce a mailbox-full condition.

Temporary mailbox thresholds were configured for testing:

```powershell
Set-Mailbox -Identity <user> `
    -IssueWarningQuota 5MB `
    -ProhibitSendQuota 6MB `
    -ProhibitSendReceiveQuota 7MB
```

Test data was then added to the mailbox to reproduce the capacity restriction.

Mailbox statistics were reviewed during the test to confirm the mailbox size and item count.

Example:

```powershell
Get-MailboxStatistics -Identity <user> |
    Select DisplayName,TotalItemSize,ItemCount
```

The controlled test reproduced the expected mailbox-full behavior, including rejection of additional incoming messages after the configured limit was reached.

## Investigation and Resolution

The troubleshooting process followed an evidence-based approach:

```text
User reports mailbox problem
        ↓
Review mailbox configuration
        ↓
Check mailbox quota
        ↓
Review mailbox statistics
        ↓
Reproduce the issue in a controlled test
        ↓
Confirm mailbox capacity restriction
        ↓
Restore the correct mailbox configuration
        ↓
Send a test message
        ↓
Verify successful delivery
        ↓
Document the resolution
```

The mailbox configuration was restored to the appropriate service limits after testing.

The final configuration used the available Exchange Online mailbox limits for the assigned Microsoft 365 license.

## Verification

After restoring the mailbox configuration, functionality was tested again.

Verification included:

- Checking mailbox quota settings
- Checking mailbox statistics
- Sending a test email
- Confirming successful delivery
- Confirming that normal mailbox functionality was restored

This demonstrated the complete troubleshooting lifecycle from investigation through verification.

## Troubleshooting Skills Demonstrated

- Exchange Online administration
- Exchange Online PowerShell
- Mailbox configuration
- Mailbox quota investigation
- Mailbox statistics
- Controlled troubleshooting
- PowerShell-based verification
- Email delivery testing
- Technical documentation

## Key Principle

**Investigate before changing configuration.**

Mailbox problems should be diagnosed using mailbox properties, quota information, statistics, and controlled testing before applying corrective changes.

esent production systems.
