% An Introduction to IT Security
% Nicolas Prigent
% January the 11th 2016

## Security and attacks in the news

- Everyday, attacks against information systems are in the news

- Many types of attackers

- Many types of objectives

- Many types of victims

## Objectives of the attackers

- Money

- Politics

- Religion

- Business

- Military 

- Personal

## Skills and resources of the attackers

- Low-level amateurs with very limited resources

- Skilled attackers with average resources 

- Nations with skilled attackers and almost unlimited resources

## Impacts on the victims 

- Money 

- Reputation and trust

- Legal

- Organizational 

## Recent example: Cryptolocker


![Cryptolocker encrypts the victim's hard-drive and asks for money for decryption. ](Cryptolocker.jpg)

## Recent example: Celebgate

![Intimate pictures of celebrities leaking on the web.](celebgate.jpg)

## Recent example: OpFrance

![OpFrance, during which groups of attackers put down French web sites following the terrorist attacks of January 2015.](opfrance.jpg)

## Recent example: ProtonMail

![DDoS attacks against Proton Mail for blackmail purposes.](protonmail.jpg) 

## Recent example: Juniper backdoor

![Inclusion of a _backdoor_ into the source code of Juniper firewalls to offer ssh access.](ssh.png) 

## What do we mean by ``security'' ? 

- _Security_ consists in enforcing that only _authorized entities_ can perform _certain tasks._ 

- The _perimeter_ of an information system is made of a set of devices, pieces of software, data and users. 

- Every information system is placed under an _authority_ that decides what is authorized and what is not. 

## Describing what is authorized 

- The _Security Policy_ defines formally or informally what is authorized, and what is not. 

- It can be based on a _white list_ (everything that is not explicitly authorized in the list if forbidden) or on a _black list_ (everything that is in the list is forbidden). 

- Enforcing the security of an information system consists in ensuring that the security policy is appropriate and enforced. 

- _Security Measures_ are deployed and maintained to enforce the security policy.  

## Security measures

Three types of security measures can be taken : 

- _Physical security measures_, that consist in physically controlling the access to components of the system. 

- _Organizational security measures_, that consist in the administrative procedures that are imposed to the users and organizations w.r.t. security. 

- _Logical security measures_, that consist in all the security measures that are implemented as pieces of software. 

While _logical security measures_ are the most common parts of IT security, the other two must also be taken seriously. 


## Security properties : C.I.A. 

The security policy is generally expressed in terms of three security properties : 

- _Confidentiality_, that means that an unauthorized entity cannot access a given piece of information or service. 

- _Integrity_, that ensures that an unauthorized entity cannot modify a given piece of information or service. 

- _Availability_, that ensures that an unauthorized entity cannot prevent a legitimate one from accessing a given piece of information or service. 

They are known as the C.I.A. properties. 

## Proof

- Another security property, _Proof_, it sometimes associated to C.I.A.

- It consists in ensuring that all the actions are traced and that traces have not been tampered with. 

- It also consists in making entities accountable, _as long as they have been authenticated_. 

## Authentication 

- Authentication consists in ensuring that an entity is who he, she or it pretends to be. 

- In the real world, your ID or your driver's license plays that role. 

- In the digital world, you can prove your identity by using something you know (a password), something you have (a credit card), something you are (your fingerprints for instance). 

- It is not, _per se_, a security property, but a _security service_. 

- One of the objectives of attackers is often to circumvent the authentication process. 

## Access control

- Access control consists in limiting the accesses of entities to services and pieces of data to authorized entities. 

- It therefore enforces the security policy, especially in terms of confidentiality and integrity. 

- It relies heavily on authentication.

- It can be coarse or fine-grained. 

## Vulnerability, threat agent, attack

- A _vulnerability_ is a weakness in a part of the system that allows an attacker to circumvent the security policy. It can for instance be the fact that a file sharing server does not perform any access control while containing confidential information. 

- A _threat agent_  is an entity which actions could breach security and thus cause possible harm. A threat agent can be, for instance, a criminal, an earthquake or a squirrel. 

- An _attack_ is a detrimental event during which a vulnerability is exploited 
(willingly or not) by a threat agent.

- Since it is very difficult to limit the threat agents, the purpose of security is to reduce vulnerabilities. 

- It is commonly admitted that is is not possible to make a system free of vulnerabilities. 


## Security is a chain

![And the attacker will focus on the weakest link](broken-link.jpg)


## Security mechanisms

Security mechanisms help enforce the security policy by reducing vulnerabilities so as to ensure security properties. 

They can act on various parts of the system : 

- On the network, 

- On the devices, 

- On the services, 

- On the data. 

_In-depth security_ consists in combining multiple security mechanisms in such a way that an attacker that succeeds in circumventing one of them will not reach his or her goals. Therefore, there is no _single point of failure_. 


## Network security

Network security consists in : 

- controlling the access to the network, 

- protecting communications, 

- filtering communications that enter and go out the network. 

Many tools and mechanisms are available to that end.

## Protecting WiFi networks

- WiFi access points allow devices to connect wirelessly to a network and possibly to the Internet. 

- When no security mechanism is implemented, anyone can connect to the network,  eavesdrop communications and inject packets. 

- WEP was first propose to prevent these. It used cryptography to enforce access control to the network as well as confidentiality and integrity of communications.

- Because WEP had its own vulnerabilities (due to bad use of cryptography), it was replaced by WPA. 

## Using VPN to secure communications between distant sub-networks 

- Companies are now located in multiple places. 

- They still need to share information and services wherever they are located. 

- Virtual Private Networks technologies such as IPsec for instance rely on 
cryptography to allow the various sub-networks to communicate securely and 
transparently, as if they were in fact a single network. 

## Protecting HTTP communications with HTTPS

- Many services can now be obtained through the web (information, social networks, banking, etc.) 

- Confidentiality and integrity of communications is necessary but is not provided by HTTP itself. 

- HTTPS is a modification of the HTTP protocol that ensures authentication of the server (and possibly of the client) as well as confidentiality and integrity of the communications. 

- It is regularly updated so as to correct vulnerabilities. 

## Firewalls

- Firewalls implement access control on networks by filtering the messages 
that go through them. 

- Historically, they looked at IP addresses and TCP/UDP ports to decide if a packet was authorized. 

- WAF (Web Application Firewalls) look at the content of web requests to enforce access control. 

## Devices security

- IT devices are numerous: personal computers, mobile phones, smart-everything, cars, but also servers and routers for instance. 

- While they are very different in size and shapes, ensuring their security is a matter of ensuring the confidentiality, integrity and availability of the services and pieces of informations they contain and access. 

- Modern devices are very complex systems for which ensuring perfect security is probably not possible. 

## Passwords, PIN codes and fingerprints

- The role of passwords, PIN codes and fingerprints is to ensure that the person 
using the device is really who he or she pretends to be. 

- Password and PIN codes must provide sufficient complexity so as not to be guessed too easily. 

- It is now considered that a good password is at least 12 characters long, with lowercase and uppercase letters, numbers and special characters. 

- Since PIN codes cannot be that complex, devices implementing them generally allow only a very small number of attempts. 

- It has been showed that fingerprint scanners can often be circumvented. 

- Your fingerprint also cannot be renewed :-). 

## What happens when you device is stolen ? 

![U.S. airports report close to 637,000 laptops lost each year](laptop-airport.jpg)

## Full disk encryption

- When a laptop is stolen, an attacker can do whatever he/she pleases with it. 

- Especially, he or she can remove the hard drive and access all the data it contains by mounting it as an external hard drive on his or her own computer. 

- Full disk encryption allows to cryptographically protect the whole disk against this. 

- In practice, full-disk encryption generally requires a password or an external 
device to boot the system. 

## Malicious software

- The purpose of malicious software is to perform malicious actions on the victim's computer. 

- _Virus_ are pieces of software that copy themselves in the other applications when the victim runs them. 

- _Worms_ spread over the network by exploiting network application vulnerabilities. 

- _Trojan Horses_ look like useful applications but perform malicious actions when launched or when some conditions are fulfilled. 

- _Phishing_ is a malicious activity during which the attacker sends malicious 
e-mails to victims so as to make them perform some actions that will compromise 
their system (run a malicious program, connect to a malicious web site, etc.)

## Anti-virus software

- _Stricto sensu_, anti-virus software analyzes the applications on the computer to detect if they contain pieces of malicious software. 

- They now offer much more features, such as scanning the received e-mails, 
verifying that the applications are up to date, etc. 

- While some of them are quite efficient, none of them can be considered bullet-proof. 

## Application vulnerabilities

- Applications can also contain implementation vulnerabilities, i.e. some programming mistakes that allow an attacker to perform malicious actions. 

- Many kinds of application vulnerabilities exist. 

- Operating systems being applications, they can contain application vulnerabilities. 

- In practice, it is almost impossible to produce an application that is free from implementation vulnerabilities. 

- Therefore, the best answer is to apply patches as soon as they are published. 

## Securing services

Since services are very different one from the others, there can't be any single way to secure them all. However, principles are always the same: 

- Careful management of users authentication. 

- Configuration of the various authorization with minimum privileges for each user. 

- Frequent deployment of patches. 

## Securing data

Data that is stored or transmitted on the network can basically be protected through to means : 

- Physical isolation of the storage of the network. 

- Protecting its integrity and confidentiality with cryptography. 


## Secure everything ? 

![Is this really a good idea ?](SecureItAll.jpg)

## Security is a trade-off

- Security costs money and time. 

- It is always possible to make something more secure, and there is no perfect security. 

- The right level of security to deploy corresponds to what will make it not worth it for the attacker to target you (and then, some :-) ).

- Security measures must focus on the relevant _risks_. 


## EBIOS, a risk analysis methodology

A _risk analysis_ is performed in order to define what should be protected, and against what. 

EBIOS (_Expression des Besoins et Identification des Objectifs de Sécurité_) is a risk analysis methodology that follows the following procedure : 

- Definition of context and perimeter

- Unwanted events analysis

- Threat scenarios analysis

- Risks analysis, based on the impact and probability of occurrence of unwanted events

- Security measures analysis

## Case study: Your Digital Life

In order to understand the EBIOS methodology, we are going to perform a risk 
analysis on the following subject: _Your Digital Life_. 
