# Security choice for encryption | Date: 13/10/25

## Context and Problem Statement
We need to choose appropriate methods for securing data in the Complaint Management System. This includes protecting stored user data and ensuring that communication between the consumer interface, staff components and backend services cannot be intercepted. Encryption is essential because the system handles sensitive personal information, and weak protection would risk data exposure, especially in a multi-tenant system where data must remain isolated.
## Considered Options
* Bcrypt hashing for passwords (Selected)
* HTTPS/TLS for data in transit (Selected)
* Database-level encryption (Transparent Data Encryption)

## Decision Outcome
Bcrypt hashing was selected for passwords because it is an OWASP-recommended one-way hash function that protects user credentials even if the database is compromised.
HTTPS/TLS was selected to encrypt all communication between the web application and backend services, reducing the risk of interception or tampering.

Database-level encryption (TDE) was considered but not required for the proof of concept, as the main security goals are password protection and safe transmission.

### Consequences
**Positive**
* Meets OWASP recommendations for Cryptographic Failures (A04:2025).
* Supports multi-tenancy by ensuring tenant data cannot be intercepted.
* Lots of support for ASP.NET and Microsoft SQL Server

**Negative**
* Bcrypt hashing is slower than basic hashing algorithms, which may increase login processing time slightly.
* Future integration with an external company’s authentication or security system may require changing or extending the current encryption approach, depending on their requirements.

### References
https://owasp.org/Top10/2025/0x00_2025-Introduction/
