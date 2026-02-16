2024-10-02 19:42

Tags: [[Security]] [[CompTIA]] [[Fundamentals]] [[Security Attacks]] [[Encryption]] [[Certificates]]

# Security+ Chapter 10 Understanding Cryptography and Public Key Infrastructure

## Providing Integrity with Hashing

Hashing verifies integrity for data both on systems and the internet. A hash is a hexadecimal number created with a hashing algorithm.

### Hash-based Message Authentication Code

Hashing is a one way function that creates an alphanumeric string of characters. It cannot be reversed.  Passwords are often hashed and stored as hashes. Additionally, an added layer of protection is to salt hashed with extra characters before hashing them. 

### Hashing Messages

If you can memorize hashing algorithms such as MD5, SHA, and HMAC, it will help you answer some questions. Hashing algorithms don't encrypt data. Encryption aims to protect data confidentiality, allowing only authorized parties to access the original information. Hashing is primarily used to verify data integrity and authenticity. Encryption produces cipher-text that varies in size based on the input. Hashing always produces a fixed-size output (hash value) regardless of input size.

## Understanding Password Attacks

### Password Spraying Attacks

Online attacks guess the password of an online system. Offline attacks guess the password within a downloaded  file, such as a database. Logs will show a large volume of failed attempts. Event ID 4625 indicates logon attempts and Event ID 4740 indicates accounts that are locked out. Spraying attacks attempt to avoid lockout policies. Logs will still show attempts. 

#### Pass the Hash Attacks

Passwords are typically stored as hashes. A pass the hash attack attempts to use a hash that was intercepted in transit. These attacks can be detected as Event 4624 with a login process of NMLMSSP and/or an Authentication Package of NLTM. 

### Birthday Attacks

Birthday attacks exploit collisions (duplicates) in hashing algorithms. A collision is a duplicate in hashes from different input. Salting adds random text to passwords before hashing them. This can also prevent rainbow table attacks (using hashes of common passwords to gain access). 

### Key Stretching

Bcrypt, PBKDF2, and Argon2 are key stretching techniques that prevent brute force and rainbow table attacks. They salt the password with additional bits and then send the result through a cryptographic algorithm.

Encryption provides confidentiality and ensures the authorized viewing of data. This applies to any data at rest (data that is stored) or data in transit (data being sent).

### Symmetric Encryption 

Symmetric Encryption uses the same key for encryption and decryption. The same key is used at both ends of the transmission media. 

### Certificates

Digital Certificates include public keys along with other details on the certificate owner and the **Certificate Authority** (**CA**). Certificate owners share their public key when sharing a copy of their digital certificate. 

### Obfuscation 

Stenography, tokenization, and masking are all examples of obfuscation. Stenography hides messages or data within other files. Tokenization replaces the data with non--sensitive tokens, retaining essential information without revealing the hidden data. Masking conceals part of the data with characters, symbols, or other data. 

## Using Cryptographic Protocols

Knowing which key encrypts and which key decrypts is essential for understanding asymmetric encryption. For example, knowing that the private key is encrypting, you know that it is being used for digital signature. 

### Protecting Email 

#### Signing Email  with Digital Signatures 

A digital signature is an encrypted hash of a message. The sender's private key encrypts the hash to create the digital signature. The receiver uses the senders public key to decrypt the digital signature and reveal the message. If successful, it provides authentication, non-repudiation, and integrity.

#### Encrypting Email

The recipient's public key encrypts when encrypting  an email and the recipient's private key is used to decrypt an encrypted email message. 

### HTTPS Transport Encryption

TLS is the replacement for SSL. TLS requires certificates issued by the certificate authorities (**CA**s). TLS encrypts HTTPS traffic, but it can also encrypt other traffic. 

#### Downgrade Attacks on Weak Implementations 

Admins should disable weak cipher suites and weak protocols on servers. When a server has both strong and weak cipher suites, attackers can launch downgrade attacks by passing the strong cipher suite and exploiting the weaker cipher suite. 


## References




