2024-09-07 01:02

Tags: [[Security]] [[CompTIA]] [[Fundamentals]] [[Security Attacks]]

# Security+ Chapter 6 Comparing Threats, Vulnerabilities, and Common Attacks'

## Understanding Threat Actors

### Threat Actor Types

An **Advanced Persistent Threat** (**APT**) is an organized and sophisticated group of attackers. Governments sponsor them and give them targets. Organized crime groups are individuals involved in crime. They are motivated by money. 

An **unskilled attacker** uses existing scripts to launch attacks. They have little expertise, sophistication, and funding. A **hacktivist** launches attacks to further a cause. An **insider** is anyone with legitimate access to an organization's internal resources (**Ex**. employee). DLP solutions can prevent users from writing to external drives. 

### Attacker Attributes

Different types of attackers have different attributes. The major differences are internal vs. external, the resources and funding available, and the attacker's level of sophistication.

### Threat Actor Motivations 

You need to know the common threat actor motivations for the exam. These include, data exfiltration, service disruption, blackmail, financial gain, philosophical belief, politics, ethical hacking, revenge, espionage, and war. 

### Threat Vectors and Attack Surfaces

Attackers use many different threat vectors to gain access to an org. So far we've discussed message-based, image-based, and file-based as well as voice calls, removable devices, vulnerable software, unsecure networks, open service ports, default creds, and the supply chain. 

### Shadow IT

**Shadow IT** refers to unauthorized systems or applications used within an org without authorization.

## Determining Malware Types

### Logic Bombs

A **logic bomb** executes in response to an event, such as when an application launches or a specific time arrives. 

### Trojans

A **Trojan** appears to be something useful but also includes malicious code, such as installing a backdoor. Many trojans are delivered via drive-by downloads. They can also infect systems with malicious software, such as fake anti-virus software, pirated software, games, or browser extensions.

### Keyloggers

**Keyloggers** capture a user's keystrokes. They are stored in a file that can be sent to an attacker or manually retrieved. **Spyware** monitors a user's computer and often includes a keylogger. 

### Rootkits

**Rootkits** have system-level or kernel access and can modify system files at the root level. Rootkits hide their running processes to avoid detection with hooking and masking techniques. Tools that can inspect RAM can discover these hidden hooked processes, but it is not guaranteed. 

### Ransomware

Ransomware is a type of malware that takes control of a user's system or data. Attackers then attempt to extort the user for money by demanding a ransom. Attackers' targets for this type of attack are increasingly becoming hospitals, cities, or large organizations, rather than individuals. 

Malware includes a wide variety of malicious code (**Ex**. viruses, worms, Trojans, ransomware). A virus is malicious code that attaches itself to an application and runs when the application is executed. A worm is self-replicating and doesn't require interaction. 

## Recognizing Common Attacks 

### Social Engineering and Human Vectors

Social Engineering uses social tactics to trick users into giving up information or performing actions they wouldn't normally take. Social engineering attacks can occur in person, digitally, or over the phone. 

A social engineer can gain unauthorized information just by looking over someone's shoulder. This might be in person or digitally using a camera. Screen filters can assist in obscuring people's view and help prevent shoulder surfing.

#### Tailgating and Access Control Vestibules

**Tailgating** is a social engineering tactic that occurs when one user follows closely behind another user without using credentials. **Access Control Vestibules** (also called mantraps) allow only a single person at a time. Sophisticated mantraps can identify and authenticate individuals before allowing access. Dumpster divers search through to find compromising data. This can be mitigated by shredding or burning docs.

### Message-Based Attacks

#### Phishing

Spam is unwanted email. Phishing is malicious spam. Attackers use phishing tactics to get users to provide sensitive or personal information. Links within an email can also lead users to download and install malware.  

#### Spear Phishing

A **Spear Phishing** attack targets specific users instead of using a brute force method. It can target employees or customers. Digital signatures provide assurances to email recipients about who sent an email and can reduce the success of spear phishing attacks. Whaling targets high-level executives or impersonates them.  

#### Vishing

**Vishing** is phishing over the phone or using VoIP. Some of these are fully automated.

## Blocking Malware and Other Attacks

### Antivirus and Anti-Malware Software

Antivirus software detects and removes malware. This includes viruses, Trojans and worms. Signature-based antivirus software detects known malware based on signature definitions. Heuristic-based antivirus software detects previously unknown malware based on behavior.

### Why Social Engineering Works

Many of the reasons that social engineers are effective is because the use psychological techniques including impersonating authority, intimidation, faking scarcity, using urgency, using familiarity, and creating a sense of trust. 

## References


