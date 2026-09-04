# Microsoft Entra ID Administration

This lab demonstrates practical Microsoft Entra ID administration and identity troubleshooting in a controlled Microsoft 365 environment.

The objective is to review user identity information, investigate authentication activity, analyze sign-in failures, and use available evidence to assess potential security concerns.

## Identity Administration

Microsoft Entra ID provides cloud-based identity and access management for Microsoft 365 users and services.

Administration and troubleshooting activities in this lab included:

- Reviewing user identities
- Investigating sign-in activity
- Reviewing authentication results
- Examining sign-in details
- Reviewing device and browser information
- Reviewing source location information
- Assessing authentication failures

## Sign-In Investigation

Microsoft Entra sign-in logs were used to investigate suspicious authentication activity reported for a test user.

The investigation focused on:

- Sign-in status
- Error code
- Source IP address
- Approximate location
- Device information
- Browser information
- Authentication method
- Conditional Access result

Example investigation workflow:

```text
Suspicious sign-in reported
        ↓
Identify affected user
        ↓
Review Entra sign-in logs
        ↓
Check authentication result
        ↓
Review error code
        ↓
Review source location
        ↓
Review device and browser
        ↓
Assess security impact
        ↓
Document findings
```

## Authentication Failure Analysis

The investigation demonstrated how authentication details can be used to determine whether a reported sign-in represents successful access or a failed authentication attempt.

Important evidence includes:

| Evidence | Purpose |
|---|---|
| Sign-in status | Determine whether authentication succeeded or failed |
| Error code | Identify the reason for authentication failure |
| IP address | Identify the source of the request |
| Location | Provide geographic context |
| Device | Identify the device used |
| Browser | Identify the client used |
| Authentication method | Determine how authentication was attempted |
| Conditional Access | Review applicable access-policy information |

A failed authentication attempt does not by itself confirm that an account has been compromised. The available evidence should be reviewed before reaching a conclusion.

## Security Investigation Example

A controlled lab investigation was performed after suspicious authentication activity was generated for a test account.

The sign-in investigation showed failed authentication attempts with invalid username/password errors.

Additional sign-in information was reviewed, including source location, device, browser, authentication method, and Conditional Access information.

The investigation demonstrated an evidence-based approach to determining whether unauthorized access had actually occurred.

## Investigation Principles

When investigating suspicious authentication activity:

1. Identify the affected account.
2. Review the sign-in event.
3. Determine whether authentication succeeded.
4. Review the error code.
5. Examine source and device information.
6. Assess the available evidence.
7. Take containment action if required.
8. Document the findings.

Security response should be proportional to the evidence and severity of the event.

## Skills Demonstrated

- Microsoft Entra ID administration
- Cloud identity management
- Sign-in log investigation
- Authentication troubleshooting
- Security event analysis
- Device and browser analysis
- IP and location analysis
- Evidence-based investigation
- Security incident documentation

## Lab Disclaimer

This is a personal hands-on Microsoft 365 administration lab created for learning and portfolio purposes.

Security scenarios and authentication activity were performed in a controlled environment and do not represent real-world security incidents.
