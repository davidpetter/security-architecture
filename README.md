# Security architecture - Work in progress!
A compiled list of information of security principles and solutions


## Cyber security
### Information security
* Confidentiality
* Integrity
* Availability

### Privacy
* Traceability
* Linkability
* Identifyability

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
* Checksum (potentially a secret)

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
