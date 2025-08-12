# RESEARCH REPORT

# Common Network Security Threats: DoS Attacks, Man-in-the-Middle Attacks, and Spoofing

## Introduction

In today’s interconnected world, network security threats are evolving faster than many organizations can adapt. Some of the most damaging attacks exploit weaknesses in communication protocols and system configurations that were never designed with hostile actors in mind. This report explores three prevalent threats — Denial-of-Service (DoS), Man-in-the-Middle (MITM), and Spoofing — explaining how each operates, the real-world harm they have caused, and practical steps to defend against them.

## 1\. Denial-of-Service (DoS) and Distributed Denial-of-Service (DDoS) Attacks

### How it works

A DoS attack is essentially about disruption. The attacker overwhelms a system or network with so much traffic or resource requests that legitimate users can no longer access it. In a DDoS scenario, this flood comes from thousands or even millions of devices — often hijacked through malware — acting together as a botnet. Attackers may exploit bandwidth limitations, target weaknesses in TCP/IP protocols, or send application-level requests that consume all server processing capacity.

### Impact

The most obvious effect is downtime. Websites go offline, services become unreachable, and business operations grind to a halt. Beyond the immediate outage, companies face lost revenue, reputational damage, and sometimes contractual penalties if service level agreements aren’t met.

### Real-world example

In October 2016, a massive DDoS attack struck Dyn, a major DNS provider. The attack leveraged the Mirai botnet, which had compromised thousands of poorly secured Internet of Things (IoT) devices. As a result, major platforms like Twitter, Netflix, and Spotify experienced outages, revealing just how dependent the internet is on key infrastructure providers.

### Mitigation measures

\- Use content delivery networks (CDNs) and DDoS mitigation services to absorb excess traffic before it reaches your servers.  
\- Configure servers with connection limits, SYN cookies, and intelligent load balancing to reduce the impact of floods.  
\- Disable or restrict unnecessary services that can be abused for amplification attacks (e.g., open DNS resolvers).  
\- Establish incident response procedures with ISPs and cloud providers so mitigation can be activated quickly.

## 2\. Man-in-the-Middle (MITM) Attacks

### How it works

In a MITM attack, the criminal positions themselves between two communicating parties and intercepts, alters, or injects data into the conversation. This can happen at the network level through ARP spoofing, in which forged messages on a local network redirect traffic through the attacker’s system. It can also happen via compromised certificate authorities (CAs) that issue fraudulent SSL/TLS certificates, making fake websites appear legitimate.

### Impact

MITM attacks are especially dangerous because the victim often has no idea they’re being watched. The attacker can steal credentials, capture sensitive data, or alter financial transactions in real time. On a larger scale, a compromised CA could enable interception of encrypted communications for thousands of websites.

### Real-world example

One of the most famous cases occurred in 2011 when the Dutch certificate authority DigiNotar was breached. Attackers issued fraudulent certificates for popular websites, allowing them to perform covert interception of secure traffic. The breach ultimately destroyed DigiNotar’s reputation and forced it out of business.

### Mitigation measures

\- Always use strong, up-to-date encryption protocols (e.g., TLS 1.3) and enable HTTP Strict Transport Security (HSTS).  
\- Monitor certificate transparency logs for any unexpected certificate issuance related to your domain.  
\- On local networks, enable security features like DHCP snooping and dynamic ARP inspection to block spoofed ARP messages.  
\- Educate users to avoid public, unsecured Wi-Fi for sensitive transactions unless using a trusted VPN.

## 3\. Spoofing Attacks

### How it works

Spoofing involves falsifying data so it appears to come from a trusted source. The most common forms are:  
\- IP spoofing: forging the source address in IP packets to disguise the sender’s identity or redirect responses.  
\- ARP spoofing: tricking devices on a local network into sending data to the attacker’s machine instead of the intended recipient.  
\- DNS spoofing: sending false DNS responses to redirect users to malicious sites.  
\- Email spoofing: forging the “From” address to make phishing emails appear to come from trusted contacts or organizations.

### Impact

The effects range from stolen credentials to complete service compromise. In some cases, spoofing is used to make larger attacks possible ,for example, IP spoofing is a key component in many DDoS reflection attacks.

### Real-world example

DNS cache poisoning attacks have redirected thousands of users to fake banking websites, where attackers collected login credentials and personal information before victims realized they were on a counterfeit page.

### Mitigation measures

\- Implement source address verification at the network level to block spoofed packets from leaving your network.  
\- Deploy DNSSEC to ensure DNS responses are digitally signed and verifiable.  
\- Enforce SPF, DKIM, and DMARC in email systems to verify sender authenticity.  
\- Monitor networks for unusual ARP traffic and apply anti-spoofing configurations on switches and routers.

## Conclusion

DoS attacks, MITM attacks, and spoofing may take different forms, but they all exploit weaknesses in how networks handle trust and communication. Real-world incidents show that the impact can be devastating — from the temporary paralysis of global internet services to the long-term erosion of user trust.  
Defending against these threats requires a layered approach: strong encryption, secure network configurations, active monitoring, and well-rehearsed incident response plans. Technology is only part of the answer — user awareness and proactive planning are equally critical in staying ahead of attackers.