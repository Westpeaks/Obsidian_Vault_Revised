2024-10-05 15:14

Tags: [[Security]] [[CompTIA]] [[Fundamentals]] [[Security Attacks]] [[Encryption]] [[Certificates]]

# Security+ Chapter 10 Understanding Cryptography and Public Key Infrastructure Cont.

## Exploring PKI Components

### Registration Authority  and Certificate Signing Requests

You typically request certificates using a certificate signing request (**CSR**). The first step is to create an RSA private-key. The private key is the used to create a public key. You can then include the public key in the CSR and the CA will embed the public key in the digital certificate. The private key remains with you and is not shared. 

### Updating and Revoking Certificates

CAs revoke certs for several reasons. These reasons can include a private key or CA being compromised. The **Certificate Revocation List** (**CRL**) includes a list of revoked certs and is publicly available. An alternative to a CRL is using an **Online Certificate Status Protocol** (**OCSP**), which returns answers as good, revoked, or unknown.

### Validating a Certificate

**Certificate Stapling** is another alternative to OCSP. The cert presenter appends the cert with a timestamped digitally signed OCSP response from the CA. This reduces OCSP traffic to and from the CA. 

### Comparing Certificate Formats 

**Canonical Encoding Rules** (**CER**) is an ASCII format for certs and  **Distinguished Encoding Rules** (**DER**) is a binary format. **Privacy Enhanced Mail** (**PEM**) is the most used cert format and can be used for almost any cert type. **P7B** files are commonly used to share public keys. **P12** and **PFX** files are commonly used to hold private keys.

## References