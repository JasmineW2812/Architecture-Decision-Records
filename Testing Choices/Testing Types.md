# Choosing best method for authorisation | Date: 13/10/25

## Context and Problem Statement
The Complaint Management System needs to be tested to ensure reliability, usability, and correctness. Since the proof of concept involves multiple components (UI, controller logic, repository and database interactions), we must choose appropriate testing types that cover both functional and non-functional requirements.
The challenge is deciding which testing approaches will give enough coverage without overcomplicating the testing strategy for a proof-of-concept build.

## Considered Options

* Unit Testing – test individual classes/methods
* Integration Testing – test interactions between components
* End-to-End (E2E) UI Testing – simulate real user behaviour
* Manual Testing / User Acceptance Testing (UAT)

## Decision Outcome
A combination of unit testing, integration testing, end-to-end testing, and manual UAT will be used.
Unit and integration tests ensure backend code behaves correctly and consistently. End-to-end tests validate that major user flows (such as submitting or viewing a complaint) work as expected. Manual testing will be used for usability checks, acceptance criteria validation, and confirming NFRs like usability and accessibility.

### Consequences
**Positive**
* Automation tests increase reliability
* Manual UAT checks the system meets user expectations and acceptance criteria
* Helps to test NFRs e.g. usability and performance

**Negative**
* E2E tests take longer to run and require a more complex setup
* Manual testing is time-consuming and may miss edge cases if not repeated consistently

### References
