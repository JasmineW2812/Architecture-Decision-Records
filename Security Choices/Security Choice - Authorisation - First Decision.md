# Choosing best method for authorisation | Date: 13/10/25

## Context and Problem Statement
For the Complaint Management System, we need to decide how users will be authorised to access different parts of the system. The system supports several user types (Admin, Help Desk Agent, Consumer), each with different permissions and responsibilities. Only the information necessary for their role should be accessible, which is important for both security and data protection requirements.

In future implementations, a Help Desk Manager role may also be added, which would require broader access to complaints and analytics.
The problem is selecting the most suitable authorisation method that is secure, maintainable, and supports multi-tenant restrictions.

## Considered Options

* Role-Based Access Control (Selected)
* Claims-Based Authorisation
* Policy-Based Authorisation

## Decision Outcome
RBAC was chosen because it is simple to implement in ASP.NET, aligns with the proof-of-concept user roles, and works effectively alongside JWT authentication. Roles can be assigned directly to users and embedded in JWT claims, allowing fast and consistent checks in controllers and UI components.
Claims-based and policy-based authorisation offer more flexibility but introduce additional complexity that is not required for the current scope.

### Consequences
**Positive**
* Helps OWASP A01:2025 (Broken Access Control) by enforcing clear boundaries.
* Can be extended with additional roles (e.g. Help Desk Manager) without major restructuring.
* Works well with JTW tokens which are going to be used for authentication.

**Negative**
*Less flexible than full policy-based or claims-based systems.
*Complex permissions may require additional logic in the future.

### References
https://owasp.org/Top10/2025/0x00_2025-Introduction/
