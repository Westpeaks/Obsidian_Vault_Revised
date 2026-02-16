2024-09-18 23:06

Tags:  [[Security]] [[CompTIA]] [[Fundamentals]] [[Security Attacks]] 

# Security+ Chapter 8 Using Risk Management Tools

## Understanding Risk Management

### Risk Management Strategies

It is not possible to eliminate risk, but you can take steps to manage it. An org can avoid risk by not providing a service or not participating in a risk activity. Insurance transfers risk to another entity. You can mitigate risk by implementing controls. When the cost of a control outweighs the cost of a risk, the risk is typically accepted. 
#### Risk Assessment Types 

A quantitative risk assessment attaches a dollar amount to identify cost and asset values. The **Single Loss Expectancy** (**SLE**) identifies each loss's cost. The **Annualized Rate of Occurrence** (**ARO**) identifies the number of times a loss could occur in a year. The **Annualized Loss Expectancy** (**ALE**) identifies the expected annual loss from the SLE and ARO. You calculate ALE = SLE x ARO. A qualitative risk assessment use judgement to categorize risks based on likelihood and impact. 
#### Risk Analysis

A risk register is a comprehensive document noting all risks and information such as owner and severity. It includes risk scores and recommended security controls t reduce the risk scores and resolve vulnerabilities. A risk matrix plots these risks into a chart. 

## Comparing and Testing Tools

### Checking for Vulnerabilities

A vulnerability scanner can identify vulnerabilities, misconfigured systems, and lack of security controls. Vulnerability scans may be configured as passive or can be penetration tests that are intrusive and can compromise a system.

#### Credentialed vs. Non-Credentialed Scans

A false positive from a scan indicates a vulnerability from a scan. However, that vulnerability doesn't exist. Credentialed scans run under the context of a valid account and can get more detailed information on targets, such as versions of software and installed applications. They are more accurate than non-credentialed.

### Penetration Testing

A penetration test is an active test that can assess security controls and determine threat impact. It starts with gathering data and information on the target and then tries to exploit vulnerabilities using attacks.

#### Privilege Escalation

After exploiting a system, penetration testers use privilege escalation techniques to gain more access to a system. They can also gain access to other systems, which is called pivoting.
#### Known, Unkown, and Partially Known Environements

Unknown environment testers have zero knowledge of a system prior to testing. They can also have partial or full knowledge (known). 

## Capturing Network Traffic

Admins use a protocol analyzer to capture, display, and analyze packets sent over a network. This can be used for troubleshooting or detecting attacks that manipulate packets. 

## References


