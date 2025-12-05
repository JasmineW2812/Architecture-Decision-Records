# Using a relational database | Date: 27/10/25

## Context and Problem Statement
We need to choose a database that is suited to the project requirements and the service-oriented architecture. The database must support both the functional requirements (such as user login and linking complaints to the correct tenant) and the non-functional requirements, such as reliability and data consistency.

The main problem is selecting a database technology that best fits the Complaint Management System while working effectively with the chosen ASP.NET stack and multi-tenant design.

## Considered Options
* Relational database - Microsoft SQL Server (Selected)
* Non Relational - MongoDB
  
## Decision Outcome
The system will use a relational database, specifically Microsoft SQL Server. A relational model provides stronger data consistency and structured relationships, which are essential for linking users, tenants and complaints. SQL Server also integrates naturally with ASP.NET applications and Entity Framework, making development and testing more efficient.

Although SOA systems often use separate datastores per service, the proof of concept will use a single shared relational database to avoid unnecessary complexity. The design will still allow services to migrate to their own databases in the future if needed.

Non-relational databases like MongoDB were considered, but their flexibility does not outweigh the need for strong relational integrity in this project.

### Consequences
**Positive**
* Relational integrity between users, companies and complaints
* Easier development and testing due to built-in ASP.NET and EF Core support for SQL Server.
* Data consistency


**Negative**
* Not as fleible if requirements were to change in the future
* Services are more tightly coupled at the data layer until seperate datastores are introduced

### References
