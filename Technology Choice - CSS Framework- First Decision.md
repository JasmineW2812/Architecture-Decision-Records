# Decision on CSS Framework | Date: 08/10/25

## Context and Problem Statement
I have designed wireframes for the UI in Mockplus.
The problem is I need to choose if using a library would be beneficial for development, or if creating all styles from scratch is better for designing a clean, modern,and accessible interface.
Given this system is not targeting a specific demographic there is more importance on following the WCAG 2.1 guidelines (e.g. menu navigation) as users will have different levels of experience navigating web apllications.
This decision must also consider maintainability, scalability and development efficiency as well as creating an interface that works reliably for both staff and consumers.

## Considered Options

* Bootstrap (Selected)
* All custom CSS
* Tailwind

## Decision Outcome
I have chosen Bootstrap to support implementing the design.
This approach speeds up development since I won’t need to write as much CSS for designing or positioning components.
Managing less code will also make the web application easier to maintain and reduce the probability of errors.

Bootstrap provides lots of options for component styling (e.g. tables, forms, buttons),
which allows me to create a UI similar to my wireframes because these rely heavily on the use of forms.
This approach minimises the need to build components entirely from scratch, giving me more time to focus on ensuring full accessibility.

I am still writing some custom CSS to modify Bootstrap components, using a hybrid approach. This balances the flexibility of custom design with the benefits of Bootstrap.
Using CSS by itself will have hundreds more lines of code in order to create components. Furthermore, using this approach in the future could cause unnecessary CSS components needing to be created or edited if class names
were too specific. This would be more beneficial for a system that needs more unique custom components, but for this system a recognisable, simple UI (e.g. complaint forms and staff dashboards designed similarly to other sites) would improve navigation of the system and user experience.

Tailwind was not chosen because while it is highly customisable, it has a more complex HTML structure.
This could slow down development of the site because I have not used Tailwind before. Also this could make the web application more difficult to maintain in future development if a developer does not know Tailwind.

### Consequences
**Positive**
* Faster development with prebuilt components, 
* Lots more reusable designs which keeps the UI consistent
* More time to focus on accessibility

**Negative**
* May need to override using !important if there are any issues with Bootstrap when using custom CSS alongside it
* Future Bootstrap upgrades may require refactoring
* Less flexibility over HTML structure compared to all custom CSS

### References
https://getbootstrap.com/docs/5.3/getting-started/introduction/
https://v2.tailwindcss.com/docs
https://www.w3.org/TR/WCAG21/

