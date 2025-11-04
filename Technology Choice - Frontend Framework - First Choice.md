# Decision on Frontend Framework | Date: 30/10/25

## Context and Problem Statement
Having selected ASP.NET for the backend and have selected the system architecture to be Service-Oriented, I need to decide on a front-end approach. The CMS will handle complaints transactionally, where a consumer submits a complaint and a staff member responds. Real-time updates are not required, but the system must remain reliable, maintainable and scalable.

The problem is to determine whether a front-end framework is necessary or if a simpler server-render approach would better meet the system requirements while allowing focus on the backend architecture.

## Considered Options

* Razor Pages / MVC (Selected)
* Blazor
* Vue.js

## Decision Outcome
I have decided the best method given the situation is to use Razor Pages / MVC, it provides a straigtforwad way to render pages directly from the server, this aligns with the transactional process that will be used in the system. Therefore, server-rendered pages are sufficient for complaint submission and response workflows without adding unncecessary complexity.

Using Razor Pages also keeps the front-end coupled closely with ASP.NET backend which will simplify the integration of modular services. This will allow for rapid development and testing of the core functionality while maintaining a clean architecture.

Blazor could provide reusable front-end components and improve the interactivity of the web application. However, given the project timeline and priority on backend functionality, this would introduce unneceessary complexity. Blazor could be considered later for the AI chatbot or if there is changing needs with how staff interacts with customers, where Blazor could create a more dynamic front-end.

I would not use Vue.js because switching between Javascript and C# would slow down development and the interactive benefits are not essential for the system at this stage.


### Consequences
**Positive**
* Quickest way to develop, allowing focus on backend architecture and core functionality
* Simplifies integration of modular services
* Server-rendered pages align well with transactional workflows, ensuring reliablilty and maintainability

**Negative**
* Less dynamic interactivity for future features e.g. AI chatbot UI
* Tightly coupled to backend could reduce the flexibility for highley interactive front-end features

### References
https://learn.microsoft.com/en-us/aspnet/core/razor-pages/?view=aspnetcore-9.0&tabs=visual-studio
https://learn.microsoft.com/en-us/aspnet/core/blazor/?view=aspnetcore-9.0
https://vuejs.org/guide/introduction.html

