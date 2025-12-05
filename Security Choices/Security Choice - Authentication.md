# Authentication method choice | Date: 13/10/25

## Context and Problem Statement
The system is being developed using ASP.NET and we need to decide on the most suitable authentication method. For the proof of concept, the login system will not be fully
integrated with an existing company website. Instead, users will be authenticated directly within the system and the architecture is designed for future implemenation of external login or SSO.

Because the system is multi-tenant, authentication must idenify both the user and tenant they belong to. This needs a secure method to work with role based authorisation as well.

## Considered Options

* JWT-based token (selected)
* Basic authentication
* OAUTH 2.0

## Decision Outcome

JWT was chosen because it provides a stateless method for authenticating users and carrying role/tenant information inside the token. It works well with ASP.NET, supports multi-tenancy, and can easily be extended to integrate with a future SSO provider.

OAuth 2.0 was not selected for the proof of concept because it is more complex to configure and typically requires an external identity provider. Basic Authentication was rejected because it sends credentials with every request and does not meet modern security standards.

### Consequences
**Positive**
* Supports multi-tenant systems by including TenantId and roles directly inside token claims.
* Aligns with OWASP recommendations for reducing Authentication Failures (A07:2025).
* Compatible with future SSO/OAuth systems if introduced later.

**Negative**
* Requires secure storage and rotation of signing keys.
* Slightly more setup than Basic Authentication.

### References
https://owasp.org/Top10/2025/0x00_2025-Introduction/
