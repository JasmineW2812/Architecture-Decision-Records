# Using Layered Architecture | Date: 01/10/25

## Context and Problem Statement

We need to design a scalable, maintainable and user-friendly Complaint Management System providing a platform for Banking and Telecom companies to communicate issues with their customers.

The problem is choosing which architectural style would be most suited for meeting functional requirements for the system.
I will need to evaluate whether it will be better to use a monolithic approach or other.
E.g. Customer sends a complaint and Staff receiving and respoding to complaint.

## Considered Options

* Layered Architecture (Selected)
* Client-Server Architecture
* Generic Web Application Architecture


## Decision Outcome

I have chosen Layered architecture because it fits a majority of key requirements. For example, the division of layers helps to plan and design a modular system. Having the seperation of the UI (presentation layer) and Backend Logic (business layer)  will be useful for creating the resolution as it will keep code well structured and will be easier to maintain these goals outlined above in the problem statement. This approach is better suited for the Complaint Management System as it will be a medium sized project.
In addition to this a key feature is the isolation of layers which will be helpful to control the flow of data and provide more security. Which is essential given the amount of communication between staff and consumer, we need to ensure this is well protected.

Another possibility is Client-Server architecture which would have the benefit of simplicity, particularly with smaller projects. However, this would not be effective for the Complaint Management System due to the amount of users expecting to use this web application. This is because the more clients added has more of a direct impact on the web applications Performance. For example, multiple users attempting to send complaints could cause a bottleneck on the server which could lead to a failure of some of those complaints being sent which will lead to both consumers and companies dissatisfied with the efficiency and reliability of the system. 

It is important to note when deciding that this it is my first choice. According to *Fundamentals of Software Architecture*  [Richard & Ford, 2020], Layered Architecture is a good option to starting point when still looking into requirements
due to its simplicity and reliability and structured approach. I still need to look into non-functional requirements and research more about the design (c4 diagrams) to know if this is the most optimal choice to create the system.



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
