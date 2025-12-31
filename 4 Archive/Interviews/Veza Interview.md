## SSO

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

**User assignment** - Determine which users/gro
ups can access the application

**Authentication flow** - Choose SP-initiated vs IdP-initiated SSO

**Session management** - Configure session timeout and re-authentication policies

**Testing** - Always test with a pilot user before rolling out broadly

## Security Considerations

- Valid SSL/TLS certificates on all endpoints
- Signed SAML assertions to prevent tampering
- Proper certificate lifecycle management (expiration dates)
- Network connectivity between IdP and SP
- Firewall rules allowing traffic between systems

## Veza - Brief Summary

Veza is an identity security platform that helps organizations visualize and control who has access to what data across their entire enterprise environment—including on-premises systems, cloud infrastructure (AWS, Azure, GCP), SaaS applications, and non-human identities like service accounts and AI agents. [Veza](https://veza.com/)[Veza](https://veza.com/product/)

**What They Do:**

Their core technology is the "Access Graph," which maps all identities, permissions, roles, and resources across systems to answer the critical question: "Who can take what action on what data?" [Veza](https://veza.com/product/)

**Key Capabilities:**

- Unify identity and access management across fragmented tools into a single platform for visibility and control [Veza](https://veza.com/)
- Automate user access certifications and reviews, prioritizing risky access for reviewers [Veza](https://veza.com/product/)
- Detect privileged users, dormant permissions, policy violations, and misconfigurations with 500+ pre-built queries [Veza](https://veza.com/product/)
- Manage non-human identities including service accounts, keys, secrets, and AI agents [Veza](https://veza.com/)
- Automate compliance reporting for SOX, HIPAA, PCI, and other regulatory requirements [AWS Marketplace](https://aws.amazon.com/marketplace/pp/prodview-ca5m5vto3ur5w)

**Who Uses It:**

Global enterprises like Blackstone, Wynn Resorts, Expedia, Crocs, and Choice Hotels use Veza to enforce least privilege access and reduce identity-related security risks. [AWS Marketplace](https://aws.amazon.com/marketplace/pp/prodview-ca5m5vto3ur5w)[LinkedIn](https://www.linkedin.com/company/veza)

**The Value Proposition:**

Veza goes beyond traditional Identity Governance and Administration (IGA) tools by providing real-time visibility into effective permissions across all systems, enabling organizations to enforce Zero Trust principles, prevent identity-based breaches, and automate remediation workflows.

This would be particularly relevant to your interview since they're looking for IAM expertise—Veza essentially sits on top of identity providers like Okta and Azure AD to give organizations a unified view of all access and permissions.


## Questions

1. What is the team size?
2. How is core to you about running support at Veza? 
3. What are support expectations for the team? 
4. What would you want to see from someone coming onto this team in the first 30 days? 
5. What's your on-call or after-hours support rotation like? What is the primary method of support response? 
6. How do you measure performance for senior support engineers beyond typical metrics like ticket resolution time?
7. What are the most common integration challenges customers face with Veza's identity security platform?


## Links:

2025111338