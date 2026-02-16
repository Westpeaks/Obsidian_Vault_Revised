2024-05-15 09:59

Tags: [[Troubleshooting]] [[SSO]] [[LDAP]] 

# SSO

Single Sign-On (SSO) is an authentication process that allows users to access multiple applications or services with a single set of login credentials (such as username and password). Instead of requiring users to log in separately to each application, SSO enables them to authenticate once and access all authorized resources without needing to re-enter their credentials.

Here's a basic rundown of how SSO works:

1. **User Authentication**: When a user attempts to access a protected resource or application, they are redirected to an authentication server or identity provider (IdP).
    
2. **Authentication Request**: The application or service sends an authentication request to the IdP, indicating that the user needs to be authenticated.
    
3. **User Authentication**: The IdP prompts the user to enter their credentials (e.g., username and password) or may use other authentication methods such as biometric authentication, security tokens, or multi-factor authentication (MFA).
    
4. **Token Generation**: Upon successful authentication, the IdP generates a security token or session identifier, which contains information about the user's identity and authentication status.
    
5. **Token Issuance**: The IdP sends the security token back to the application or service that initiated the authentication request.
    
6. **Access Granted**: The application or service validates the security token received from the IdP. If the token is valid and the user is authorized to access the requested resource, access is granted without requiring the user to log in again.
    
7. **Session Management**: The user's authentication session may be maintained by the IdP or by the application/service itself, depending on the SSO implementation. This allows the user to access other resources or applications within the same SSO ecosystem without needing to re-authenticate.

##### To break it down simply:
- **User Accesses Application**:
    
- **Application Redirects to Identity Provider (IdP)**:
    
- **User Authentication at IdP**:
    
- **IdP Generates Security Token**:
    
- **IdP Sends Token to Application**:
    
- **Application Validates Token**:
    
- **Access Granted**:
    

Benefits of SSO include:

- **Improved User Experience**: Users only need to remember one set of credentials, reducing the number of passwords they need to manage and simplifying the login process.
    
- **Enhanced Security**: SSO can help enforce stronger authentication policies, such as multi-factor authentication, and centralized authentication allows for better control and monitoring of user access.
    
- **Increased Productivity**: Users can quickly access multiple applications or services without interruption, leading to improved productivity and efficiency.
    
- **Simplified Administration**: Centralized management of user accounts and access rights makes it easier for administrators to provision, de-provision, and manage user access across the organization.

<h2>LDAP</h2>
1. **Directory Structure**:
    
    LDAP directory structure resembles a tree, with branches and leaf nodes representing organizational units, groups, users, and other directory objects.
    
2. **Client-Server Model**:
    
    LDAP operates on a client-server model, where LDAP clients (applications or services) communicate with LDAP servers to perform directory-related operations.
    
3. **LDAP Protocol**:
    
    LDAP clients use the LDAP protocol to communicate with LDAP servers, performing operations such as search, bind, add, modify, delete, and compare.
    
4. **LDAP Queries**:
    
    LDAP clients use LDAP queries to search for directory information based on specific criteria, such as user attributes or group memberships.
    
5. **Authentication and Authorization**:
    
    LDAP servers store authentication and authorization information, including user accounts, passwords, group memberships, and access control lists (ACLs).
    
6. **LDAP Directory Services**:
    
    LDAP servers provide directory services, such as storing and managing directory information, authenticating and authorizing users, and supporting directory replication and synchronization.
    
7. **LDAP Security**:
    
    LDAP supports various security mechanisms, including TLS/SSL encryption for data in transit, SASL for authentication, and ACLs for access control.

## References


