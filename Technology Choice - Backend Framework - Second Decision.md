# Using ASP.NET (C#) | Date: 27/10/25

## Context and Problem Statement
I have finished creating C1, C2 and C3 diagrams and I am evaluating security and architectural considerations for the tech stack I will use. 
My main concern with the current choice of Laravel is being able to directly produce what I will have in the C4 diagram and translate it easily to code.
As well as changing the styling approach from Layered to Service Oriented Architecture, so I need a backend framework that supports modular service development, efficient deployment and seperation between services.
Given the CMS needs to handle large numbers of complaints, maintain transactional integrity and later integrate an AI chatbot. Laravel may no longer be the best choice for meeting the project's requirements.

The problem Laravel may no longer be the best choice for this stage of the project.

## Considered Options
* ASP.NET (selected)
* Laravel
* Node.js

## Decision Outcome
I have chosen ASP.NET as the backend framework because it is well suited for creating modular services and supports Service-Oriented Architecture. For example the Complaint Service and User Management Service can be developed, deployed and maintained independently, which is critical for a system that will be used by staff and consumers continuously.
ASP.NET also allows the class-based structure needed to directly implement the C4 diagrams, this ensures the system design maps closely to the code. 
e.g. https://github.com/ardalis/CleanArchitecture/blob/main/src/Clean.Architecture.Core/Services/DeleteContributorService.cs

While Laravel would still be capable, its model-driven approach makes translating C4 diagrams less straightforward, and its deployability is more tightly coupled across layers. Therefore, the scalability (more optimised for ASP.NET *(Soni, 2024)*)
ties direcly with requirements which are higher priority for the system. e.g. handling potentially millions of complaints.

Node.js is designed for event-driven architecture, which is not required for this system because complaints will be handled in a transactional way.
This is because a consumer sends in a complaint then a staff member responds there is no back and forth to require real-time updates.
In addition, the libraries aren’t as mature or robust as what C#/.NET offers. That could make maintaining a class-based, modular structure harder in the long run. *(Node.JS vs. ASP.NET: What to Choose in 2024?, n.d.)*

### Consequences
**Positive**
* Well documented support
* Strong security features built-in e.g. authentication and data protection both essential for banking and telecom compliance
* Direct translation from C4 diagrams to code, provides easier implementation and maintenance
* Strong reliability and scalability through supporting modular services


**Negative**
* Slightly less familiarity using C# and .NET which could slow down development
* Heavier framework, which could require more server resources for smaller resources
* Laravel has more rapid development due to simplicity

### References
Node.JS vs. ASP.NET: What to Choose in 2024? (n.d.). Www.arkasoftwares.com. https://www.arkasoftwares.com/blog/node-js-vs-asp-net/
Soni, B. (2024, July 31). Laravel vs. ASP.NET in 2024: Learn the Differences & Select the best for your project. Codementor.io; Codementor. https://www.codementor.io/@bijal/laravel-vs-asp-net-in-2024-learn-the-differences-select-the-best-for-your-project-2ipcpycgxl
https://github.com/ardalis/CleanArchitecture/blob/main/src/Clean.Architecture.Core/Services/DeleteContributorService.cs
