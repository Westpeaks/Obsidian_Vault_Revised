
Tags: [[Security]] [[CompTIA]] [[Fundamentals]] [[User Identity and Access]]
# Security+ - Chapter 2 Understanding Identity and Access Management

## Exploring Authentication Management

- **Identification** occurs when a user claims an identity, such as a username or email.
- **Authentication** occurs when the user proves the identity. 
- **Authorization** occurs when access control systems grant access to resources based on permissions granted to the identity. 
- **Accounting** provides logging. \
### Comparing Authentication Factors
Most cyber security professionals recognize three types of strong authentication factors: something you know, something you have, something you are. The fourth factor, somewhere you are, is not a strong authentication factor in and of itself. Location-based authentication is not normally used.  

#### Something You Know
Complex passwords use a mix of character types. Strong passwords use a mix of character types and are at least eight characters. Password expiration identifies when a password must be changed.

**Account lockout policies** thwart some password attacks, such as brute force and dictionary attacks. Default passwords should be changed for all applications before deployment.

#### Something You Have
Smart cards are often used for 2FA where users have something (a smart card) and know something (a pin). Smart cards include imbedded certificates used with digital signatures and encryption.

##### Hard Tokens and Soft Tokens

There are two different ways that tokens remain in sync with authentication servers:

Tokens using **HMAC-based One-Time Password** algorithm change their code based upon a moving counter. Each time a code is used, both the auth server and token use the algorithm with a shared secret key to generate the next code. Since they have the same secret, they generate the same code. 

Tokens using the **Time-based One-Time Password** algorithm change their code based upon the current time. You can recognize **TOTP** tokens by the fact that their code changes automatically. 

**HOTP** and **TOTP** are open-source standards used to create one-time passwords. 

#### Something You Are

The third factor of authentication (something you are, defined with biometrics) is the strongest individual authentication factor. Biometric methods include fingerprint recognition, vein pattern matching, retinal and iris scans, facial and voice recognition, and gait analysis. 

Iris and retina scans are the strongest biometric methods. Iris scans are commonly preferred over retina scans. Retinal scans are intrusive and may reveal private medical concerns. Facial recognition and gait analysis can also be used bypass enrollment when used for identification (**Ex**. casinos).

#### Two-factor and Multifactor Authentication

Using two or more methods in the same factor of authentication (such as a PIN and a password) is single-factor authentication. Two-factor authentication uses two different authentication factors. Multi-factor authentication uses two or more factors.

#### Passwordless Authentication

Passwords are one of the least secure ways to authenticate. Passwordless authentication is not necessarily multifactor authentication. You can still use single-factor authentication in passwordless authentication methods.

## Managing Accounts

### Privileged Access Management

Privileged Access Management (PAM) systems implement stringent security controls over accounts with elevated privileges such as administrator or root-level accounts. Some capabilities include allowing users access to the administrator account without knowing the password, logging all elevated usage, and automatically changing the admin password. 

### Prohibiting Shared and Generic Accounts

Requiring admins to use two accounts, one with admin privileges and one with user privileges, helps prevent privilege escalation attacks. Users should also not use shared accounts.

### Deprovisioning

An account disablement policy identifies what to do for employees who leave permanently or are on a leave of absence. Most policies require an admin to disable an account as soon as possible. This ensures that users are unable to use the account but data associated with it (**Ex**. security keys) remains intact. Deleting an account will delete the associated data. 

### Account Audits

Usage auditing records user activity in logs. A usage auditing review looks at the logs to see what users are doing and it can be used to re-create an audit trail. Permission auditing reviews ensure that users have only the access they need to perform their jobs and prevent privilege creep issues.  
## References


