# Using a relational database | Date: 27/10/25

## Context and Problem Statement
We need to choose a database that is most suited for the project and architectural style. The database needs to fit both functional and non functional requirements for the proof of concept the key ones related to this include reliability, a method for user login and linking a consumer's complaint to the company. 

The problem is selecting the database that will be the most beneficial for the Complaint Management System that will communicate well with the SOA architecture

## Considered Options
* Relational database - MySQL centralised usage
* Non Relational - MongoDB
  
## Decision Outcome
The system will be built using a single relational database as the system will have better data consistancy given the structured relationships
e.g. link between user and complaint. While it is common to have multiple databases for SOA, for the proof of concept in order to not overcomplicate the system it will be singular. This will help with testing the backend of the services. 
It will however still be implemented in a way so servers are able to migrate to there own datastores in the future if needed.

While a non relational database such as MongoDB would offer flexibility and better scaling the relational integrity is better required for linking users to other tables

### Consequences
**Positive**
* Relational integrity between users, companies and complaints
* Easier to develop and testc a
* Data consistency


**Negative**
* Not as fleible if requirements were to change in the future
* Services are more tightly coupled at the data layer until seperate datastores are introduced

### References
