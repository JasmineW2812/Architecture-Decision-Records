# Title Decision on Frontend Framework | Date: 30/10/25

## Context and Problem Statement
Now I have selected a backend framework and reviewed functional and non-functional requirements, C4 diagrams, and UI design/libraries. 
I need to compare and evaluate the use of a front-end framework to see if it will be beneficial and support Service-Oriented Architecture.
However, it may not be necessary if the benefits are not significant, given that we need to prioritise the backend. Another consideration is the time required to develop the system.

The problem is to find out if a front-end framework would be useful enough for development or if it is better to not use one.

## Considered Options

* Razor Pages / MVC - No Front-End Framework (Selected)
* Blazor
* Vue.js

## Decision Outcome
I have decided the best method given the situation is to use Razor Pages, because it requires fewer tools,
which keeps the front-end simple and easier to maintain. This is important as the complexity will be focused on the backend,
helping to keep the architecture clean and aligned with the C4 diagrams.
Server-rendered pages will be enough for the complaint system, as communication will be handled transactionally rather than in real-time.

Blazor would be more ideal if there was more time to develop the system, as it supports reusable components and scalable front-end architecture.
However, for current development, it would be too complex to manage. This could be implemented in the future since the codebase is still in C#.

I would not use Vue.js for similar reasons to the backend framework: the interactive benefits are not a priority given the transactional nature of the complaint system.
Additionally, switching between JavaScript and C# would slow development, as I have less experience with JavaScript, making it harder to efficiently manage the front-end.

Lastly, I cannot guarantee that using a framework would provide a significant performance benefit at this stage of the project.

### Consequences
**Positive**
* Quickest way to develop which is needed due to time constraints
* More focus on the backend architecture
* Does not overcomplicate architecture and keeps it clean

**Negative**
* Less dynamic interactivity
* Tightly coupled to backend could reduce the flexibility for complex client-side interactions in the future e.g. the ai chatbot

### References
https://learn.microsoft.com/en-us/aspnet/core/razor-pages/?view=aspnetcore-9.0&tabs=visual-studio
https://learn.microsoft.com/en-us/aspnet/core/blazor/?view=aspnetcore-9.0
https://vuejs.org/guide/introduction.html

