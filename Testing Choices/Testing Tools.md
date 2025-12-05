# Selecting Testing Tools | Date: 13/10/25

## Context and Problem Statement
The system requires reliable and repeatable testing across different layers: backend logic, integration points, and the user interface. We must choose testing tools that work well with the ASP.NET stack and support the testing types selected in the previous ADR. The tools should be easy to maintain and suitable for the scale of a proof-of-concept project.

## Considered Options

* NUnit
* xUnit
* MSTest
* Selenium WebDriver

## Decision Outcome
NUnit and Selenium are selected as the primary testing tools.

NUnit is chosen for unit and integration testing because of its familiarity, simple assertions, wide community support, and strong compatibility with ASP.NET projects. Selenium WebDriver is selected for end-to-end (E2E) UI testing because it allows automated browser testing, which is ideal for validating consumer workflows such as submitting and viewing complaints.

### Consequences
**Positive**
* NUnit provides a simple and expressive framework for backend tests.
* Selenium allows automated browser testing, reducing manual effort for core user flows.
**Negative**
* Selenium tests can be slower and more brittle than unit tests.
* Requires maintaining browser drivers and test environment configuration.

### References

