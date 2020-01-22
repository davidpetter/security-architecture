# Security architecture
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
* API-key
* Session ID/key
* Nonce
* Symetric cipher keys  
* Private cipher key
* Key derivation material
* Checksum hashes (potentially a secret)

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
* Etc

# MMI - Machine to machine interaction


## DNS
DNS is crucial/weak/important

The DNS is responsible for the mapping between domain names and IP adresses.
The domain name is the public identity of the server. 



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
