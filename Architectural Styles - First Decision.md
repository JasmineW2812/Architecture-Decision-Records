# Using Layered Architecture | Date: 01/10/25

## Context and Problem Statement

We need to design a scalable, maintainable and user-friendly Complaint Management System providing a platform for large companies to communicate issues with their customers.

The problem is choosing which architectural style would be most suited for meeting functional requirements for the system.

## Considered Options

* Layered Architecture (Selected)
* Client-Server Architecture
* Generic Web Application Architecture


## Decision Outcome

I have chosen Layered architecture because it fits a majority of key requirements. For example, the division of layers helps to plan and design a modular system. This is important
as the system is expected to provide a variety of functional requirements for a large user base. In addition to this a key feature of Layered Architecture is the separation of Layers,
this is beneficial as it helps us to understand where each functionality takes place. Combined with this the isolation of layers can keep data more secure which is important given there will likely be a lot of communication between consumer and support.

It is important to note when deciding that this it is my first choice. According to *Fundamentals of Software Architecture*  [Richard & Ford, 2020], Layered Architecture is a good option to starting point when still looking into requirements
due to its simplicity and reliability and structured approach. I still need to look into non-functional requirements and research more about the design (c4 diagrams) to know if this is the most optimal choice to create the system.

The main reason client server architecture would not be ideal is while it is simpler to implement and design as it is only two tiered, so it is not as modular or scalable for larger system. Furthermore, there could be future issues without separating component interactions.

The issue with Generic Web Application is the lack of separation of concerns so extending with future requirements of adding a chatbot could be more difficult due to a lack of modularity.

### Consequences
**Positive**
* Modular and reusable components
* Improved data security through layer isolation
* Easy to make a well-structured design

**Negative**
* Risk for sinkhole anti-pattern e.g. too many layers can impact performance
* Potentially further decomposition needed due to complexity

### References
Richards, M., & Ford, N. (2020). Fundamentals of software architecture : an engineering approach. O’reilly.

‌
