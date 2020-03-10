# Security architecture - Work in progress!
A compiled list of information of security principles and solutions

## Cyber security
### Information security
#### Confidentiality
Guarding against improper information modification or destruction, and includes ensuring information nonrepudiation, accuracy, and authenticity.

Safeguards: Access control & protection, encryption, monitoring and training etc.

#### Integrity
Preserving authorized restrictions on access and disclosure, including a means for protecting personal privacy and proprietary information.

Safeguards: Encryption, signature, process control suchs as code testing, monitoring control sucn as message and data integrity and log analysis. Behavioral controls such a separation fo duties, rotation of duties and training etc.

#### Availability 
Ensuring timely and reliable access to, and use of, information (failure to operate due to failure, loss, error, prevention or overload).  

Safeguards: access controls, monitoring, data and computational redundancy, resilient systems, virtualization, server clustering, environmental controls, continuity of operations planning, and incident response preparedness etc.

### Privacy
* Traceability - Ability to trace the object (information) from origin to destination
* Linkability - Abilltiy to link to objects (information) going either from/to the same origin/destination.  
* Identifyability - Ability to ident

## Threat sources
Information security is about blocking or reducing damage to confidentiality, integrity, and availability of information and systems.

Damaged cause from one or more of the threat sources:
* Hostile cyber or physical attacks
* Human error
* Structural failures of organization-controlled resources (e.g., hardware, software, environmental controls)  
* Natural and man-made disasters, accidents, and failures beyond the control of the organization

## Application security principles
* Apply defense in depth
* Use a positive security model (fail-safe defaults, minimize attack surface)
* Fail securely
* Run with least privilege
* Avoid security by obscurity (open design)
* Keep security simple (verifiable, economy of mechanism)
* Detect intrusions (compromise recording)
* Don’t trust infrastructure
* Don’t trust services
* Establish secure defaults (psychological acceptability)

## Secrets

Types of Secrets
* Password (all forms plain, hash etc)
* Token (API-key, Session ID/key)
* Keys (private cipher keys and derivation material)
* Hashing pepper
* Checksum and hashes (potentially a secret)
* Secret data

Principles
* High entropy - Prefer long and random over strict limitations
* Keep secrets safe and seperate from other code or data
* Have a short lifecycle
* Don't rely on one kind of secrets for all your security

## Trust
In the end security relies on trust. A solution will most likely have several different
trust anchors such as:
* Identity provider
* CA in a PKI based solution.
* Peer in web of trust.
* Identity card issuer
* Co-worker at work
* Etc

### Segregation of duties
The concept of having more than one person required to complete a task.
In business the separation by sharing of more than one individual in one single task is an internal control intended to prevent fraud and error.

Principles
* There should be a determined set of trust anchors 
* There should be a lowest level of acceptable trust
* There should be a chain of trust from a trust anchor
* Chain of trust should verifiable
* Broken chains or chains that don't meet criteria should not be trusted

# MMI - Machine to machine interaction


## DNS
DNS is crucial/weak/important

The DNS is responsible for the mapping between domain names and IP adresses.
The domain name is the public identity of the server. 

Design
* Use DNSsec for authenticating DNS records 
* OverConsider haHave failover and zoning

## TLS
TLS is a protocol for channel security. 
Correctly configured enables verification of the server via the domain name.

Trust anchors
* DNS 
* CA (certificate authority).

Weakness
* Options, variants, versions and configurations

Best practice
* Always use TLS (almost always anyway)
* Use secure protocols and ciphers
* Use a public trusted CA
* Secure the DNS (with DNSsec etc)
* Use forward secrecy
* Use full certificate chains
* Strong private key
* Secure private key
* Disable insecure renegotiation

Links
* https://github.com/ssllabs/research/wiki/SSL-and-TLS-Deployment-Best-Practices


## REST, SOAP, GRPC etc.

## File transfer (FTP etc)

##

# HMI - Human to machine interaction

# HHI - Human to human interaction

# Runtime security
## Backend
## Client
### Browser
HTTP headers:
https://www.keycdn.com/blog/http-security-headers



# Links
[DevSecOps](http://devsecops.github.io/)
