# Using Laravel (PHP) to build the application | Date: 01/10/25

## Context and Problem Statement
We need to choose a backend framework to build the application following Layered Architecture. To support the
architecture, it must allow for modular development, data isolation between layers and integration of multi-tenancy.

The problem is choosing a backend which will integrate well with the designs (c4 created at a later date) and
will likely meet all the requirements expected of the software.

## Considered Options

* Laravel (selected)
* Django 

## Decision Outcome
I have chosen Laravel for the backend as it fits well with the Layered Architecture approach.
Laravel uses a Model View Controller structure, which helps separate the different layers and makes the system easier to manage and improve in the future.
This structure supports modularity and keeps each layer isolated from the others.

I also have more technical experience working with Laravel, such as setting up secure databases and using Laravel APIs for email connections.
In addition from knowing the framework already, it should help speed up development and let me focus on making the application more reliable and high quality. Along with this, I would be more confident on
creating a database and models in laravel that support multi-tenancy.

While Django is a popular framework, I’m not as comfortable using Python for backend development this could risk progress not being made in the time expected. Django can be modular through its app structure, but
by default because it is more common to put multiple functionalities within one app, which can make a layered approach more difficult for me to learn for the first time using Django.

### Consequences
**Positive**
* Modular structure
* Maintains data integrity between layers
* Faster development due to familiarity using the framework 
**Negative**
* Fewer framework tutorials and documentation compared to more widely used options
* Readability could be an issue for future developers unfamiliar with PHP

### References
https://laravel.com/docs/12.x
https://docs.djangoproject.com/en/5.2/
‌
