 ## Prerequisites

**On the Identity Provider (IdP) side:**

- Administrative access to your IdP (Okta, Azure AD, etc.)
- Ability to create and configure applications
- Access to generate/manage certificates for SAML signing
- Domain ownership verification (for some configurations)

**On the Service Provider (SP) side:**

- The application must support SSO (SAML 2.0, OAuth 2.0, or OpenID Connect)
- Administrative access to configure authentication settings
- Understanding of the app's SSO implementation

## Essential Information Exchange

**From the Service Provider, you'll need:**

- **ACS URL** (Assertion Consumer Service URL) - Where the IdP sends authentication responses
- **Entity ID** or **Audience URI** - Unique identifier for the application
- **SP Certificate** (if using encrypted assertions)
- Supported SSO protocols and bindings

### ==From the Identity Provider, you'll provide:==

- ==**IdP Metadata URL** or XML file containing:==
    - ==SSO endpoint URLs==
    - ==IdP Entity ID==
    - ==X.509 signing certificate==
- ==**Sign-in URL** - Where users are redirected to authenticate==
- ==**Sign-out URL** (optional but recommended)==

## Configuration Steps

**Attribute mapping** - Map IdP user attributes to what the SP expects (email, username, firstName, etc.)

**User assignment** - Determine which users/groups can access the application

**Authentication flow** - Choose SP-initiated vs IdP-initiated SSO

**Session management** - Configure session timeout and re-authentication policies

**Testing** - Always test with a pilot user before rolling out broadly

## Security Considerations

- Valid SSL/TLS certificates on all endpoints
- Signed SAML assertions to prevent tampering
- Proper certificate lifecycle management (expiration dates)
- Network connectivity between IdP and SP
- Firewall rules allowing traffic between systems


## Links:

2025111322