# Using ASP.NET (C#) | Date: 27/10/25

## Context and Problem Statement
I have finished creating C1, C2 and C3 diagrams, I am evaluating security and architectural considerations for the tech stack I will use. 
My main concern with the current choice of Laravel is being able to directly produce what I will have in the C4 diagram to translate easily to code.
As well as changing the styling approach from Layered to Service Oriented Architecture, there is potentially a better option to creating modular services.

The problem Laravel may no longer be the best choice for this stage of the project.

## Considered Options
* ASP.NET (selected)
* Laravel
* Node.js

## Decision Outcome
I have chosen ASP.NET as the backend framework because it is well suited for creating modular services and would be better for implementing Service-Oriented Architecture through examples. e.g. https://github.com/ardalis/CleanArchitecture/blob/main/src/Clean.Architecture.Core/Services/DeleteContributorService.cs

It is also well documented and widely used which will ensure maintainability and security features that can easily be implemented.
Lastly, it fixes the issue of being easier to translate the C4 diagram because we can directly create classes that interact with the data instead of models.

While Laravel would still be capable, using C4 diagrams will not be as straightforward this is because the data is mainly communicated through models rather than directly via classes. Also non-functional requirements such as
scalability and performance is far more optimised for ASP.NET. *(Soni, 2024)*

Node.js is better for event driven architecture, which is not the architecture we are using or need as complaints will be handled in a transactional way.
This is because a consumer sends in a complaint then a staff member responds there is no back and forth to require real-time updates.
In addition, the libraries aren’t as mature or robust as what C#/.NET offers. That could make maintaining a class-based, modular structure harder in the long run. *(Node.JS vs. ASP.NET: What to Choose in 2024?, n.d.)*

### Consequences
**Positive**
* Well documented support
* Strong security features built-in e.g. authentication and data protection
* Closer translation from C4 diagrams to code
* Strong performance and scalability


**Negative**
* Slightly less familiarity using C# and .NET which could slow down development
* Heavy framework, which could require more server resources for smaller resources
* Laravel has more rapid development and simplicity

### References
Node.JS vs. ASP.NET: What to Choose in 2024? (n.d.). Www.arkasoftwares.com. https://www.arkasoftwares.com/blog/node-js-vs-asp-net/
Soni, B. (2024, July 31). Laravel vs. ASP.NET in 2024: Learn the Differences & Select the best for your project. Codementor.io; Codementor. https://www.codementor.io/@bijal/laravel-vs-asp-net-in-2024-learn-the-differences-select-the-best-for-your-project-2ipcpycgxl
https://github.com/ardalis/CleanArchitecture/blob/main/src/Clean.Architecture.Core/Services/DeleteContributorService.cs
