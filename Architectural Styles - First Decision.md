# Using Layered Architecture

## Context and Problem Statement

We need to design a scalable, maintainable and user-friendly Complaint Management System providing a platform for large companies to communicate issues with their customers.

The problem is choosing which architectural style would be most suited for meeting functional requirements for the system.

## Considered Options

* Layered Architecture (Selected)
* Client-Server Architecture
* Generic Web Application Architecture


## Decision Outcome

I have chosen Layered architecture because it fits a majority of key requirements. For example, the division of layers helps to plan and design a modular system. This is important
as the system is expected to provide a variety of functional requriements for a large user base. In addition to this a definitive feature of Layered Architecture is the seperation of Layers,
this is beneficial as it helps us to understand where each functionality is taken place along with the isolaion of layers can keep data more secure which is important given there
will likely be a lot of communication between consumer and support.

It is also important to note when deciding this since this is my first choice, as recommended in [ ] this is a good option to starting point when still looking into requirements
due to its simplicity and reliablity + structure. I still need to look into non-functional requirements and research more about the design (c4 diagrams) to know if this is the
most optiomal design to help me create this.

The main reason client server architercture would not be ideal is potential risks due to network dependency where poor connectivity can lead to performance issues which could
risk non-functional requirments not being met. (e.g. availability)

The issue with Generic Web Application is the lack of a clear structure which when creating a medium to large sized web-application can cause unexpected issues during development
as a modular approach may not have been planned.


### Consequences

* Good, because  Modular, Reusable, Ease of Maintenance, Isolation
* Bad, because - More modular may be needed, Risk for sinkhole anti-pattern
