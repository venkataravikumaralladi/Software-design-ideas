### Domain Driven Design (DDD)

Domain-driven design is even more important for software architects, and even more so for aspiring software architects. Its strategic design decision tools will 
help you decompose a large system into components—services, microservices, or subsystems—and design how the components are integrated with one another to form
a system.

The `domain` is a fancy way of saying the problem you’re trying to solve. Depending on which system you’re talking about about, the domain might be online reailer,
purchasing and procurement, or product design, or logistics and delivery, industrial product, bank product etc.  Software developer spend their days trying to
improve or automate business processes physically happening in real time world in secured and safety manner ; the domain is the set of activities that those
processes support. A `model` is a map of a process or phenomenon that captures a useful property. The `domain model` is the mental map that business owners have of their businesses. 

Domain-driven design will make you a more effective software engineer by alleviating the process of making sense of business domains and guiding the design decisions according to the business strategy. The `tighter` the `connection` between the `software design` and its `business strategy` is, the easier it will be to maintain and evolve the system to meet the future needs of the business, ultimately leading to more successful software projects.

#### DDD theme

Effective communication is the central theme of the domain-driven design tools and practices. Domain driven design is all about

  1. Colloborative process i.e., business people and developers work together daily through out the process.
  2. Build on notion of modeling: basic idea is structure of the code should model or map the structure of the domain with in which problem is being solved. Idea is that business user should able to understand the overll structure of the software system and make sense of it. This will help us if changes are made to domain, which maps to where code changes should occur. So if there is `one to one` mapping between code and domain, when a change happens in the domain, developer know exactly where to look in the code in order to make the change.
  3. We cannot do DDD if we don't have business people in the room, i.e., business people will contribute to architecture and code than technical people because if you analyze the domain, you are analyzing the code. `The structure of the doamin is the strucutre of the code.`
  4. Microservies are all modeled around the business concepts and that's what DDD is all about.

#### Parts of DDD

DDD can be divided into two parts: strategic and tactical.

The strategic tools of DDD are used to analyze business domains and strategy, and to foster a shared understanding of the business between the different stakeholders.
We will also use this knowledge of the business domain to drive high-level design decisions:decomposing systems into components and defining their integration patterns. The `strategic` aspect of DDD deals with answering the questions of `“what?”` and `“why?”` —what software we are building and why we are building it. There is no sense in talking about the solution before we agree on the problem, and no sense talking about the implementation steps before we agree on the solution. So we perform `strategic` aspect of DDD. To design and build an effective solution, you have to understand the problem. The problem, in our context, is the software system we have to build. To understand the problem, you have to understand the context within which it exists—the organization’s business strategy, and what value it seeks to gain by building the software.

Domain-driven design’s tactical tools address a different aspect of communication issues. DDD’s `tactical patterns` allow us to write code in a way that reflects
the business domain, addresses its goals, and speaks the language of the business. The tactical part is all about the “how”—how each component is `implemented`.

#### DDD structures and terminology

When you are thinking about DDD, it is about organizing code along certain well-defined boundaries.

1. `Bounded contexts`: It is a natural division within a business. Example: context is book store (purpose is deal with the sales), and there is another context in order for book store to work is for example another context is "book ware house" (purpose is deal with delivering). This is important i.e., thinking in terms of purpose and responsbilities will help us to keep contexts seperate from each other i.e., think in terms of what are the responsbilities of the people working in that context. To communicate between contexts we create a seperate module which talks to outside world of context.

In DDD we move away from relational data base thinking. In RDBMS thinking we try to make giant components, if you will, that could be used every where which is considered bad thing in DDD world to have a single product object that could be used in multiple contexts.

2. `Entity`: An entity is an individual with in a given context. So entity is much like an object/class in object oriented world, it has one job and does one thing and does that one thing in that specific context. Roles are considered in context of entities. See `Roles` notes section below. `Entities are the roles that the person takes on as they are actually doing work`.

3. `Aggregate`: An aggregate is a collection of entiteis you talk to through a single portal.

4. `Ubiquitous language`: The idea of the ubiquitious language is that within a given context, the people who are working in that context use a language of their own and the language of one context is difffernt from the language in other contexts. For example in book store context when we are talking about book, what you care about are things that are relevant to the responsibility of the people who are working in that context, in other words, they are relevant to sales. So if you are thinking about the book, the language of books is going to talk about things like authors, reviews, readability and length and stfff that a reader would be interested in when you are trying to sell a book to them. On the ware house context side, the language, the definition of a book is different because you don't really want to sell it anymore, here language of books involves weight, size, things that are of interest to people that are taking books and putting them into boxes and sending them off to people. So this differences occur not just noun level but also at verb level, in other words, the things that you do do books is different, depending on which context you are in and those things are captured in the language, So on the sales side you sell books obviously or you shelf books or you organize books. Over on ware-house side, you pick books off the shelves and you box the books and soon and so forth. The languages are different.  Formalizing ubiquitious languages is an important part of DDD, `the basic idea here is that language itself will be reflected in the code`

  So the words that are used to describe a book will be different with in the ware house context than they are with in the store context. So as a consequence when     you implement , the namess of things will be different is that ware-house kinds of names will be used on the ware house side and book kinds of names will be used   on book store. 

  So this is ubiquitious langauge that reflects at every level. `It is the lanaugage that you programmer or architect will be using as you talk about the problems you are solving.` It is langauge that is reflected in the code itself, in that that will provide names for things that appear in the code. And it's a language that is going to be used at the domain level itself in order to describe the work that's going on. So it is ubiquitious, but it is ubiquitious within a specific context.

One the great tests to see whether something belongs in a context or not is to look at the way that you describe that something and see which langauge is most appropriate for that someghing.

5. `Roles`: Another critical thing to bear in mind when we are talking about `entities` is distinguish between actors (people) and roles (tasks) is that we talk about roles that people take on as they are working, not the actor, nor the person who is in that role. For example in time sheet system a manager authorizes timesheets that is a role, and employee fills out timesheet that is the role, here no where do you need to be both a manager and an employee, in other words, the fact that a manager is an employee in the realworld is irrelevant with respect to domain driven design. What we care about is the roles. The fact that an individual person sometimes login to the system in the role of manager in order to authroize timesheets, and that other times, the same person logs onto the system in the role of employee to fill out a time sheet, is irrelvenat from the point of view of design, as fare as we are concerned they are seperate people.  Actors may accomplish tasks in different roles. Ubiquitious languge tries to identify roles for entities. So one of the things that we are doing with the ubiquitious language is trying to identify roles that people take on as the stories play out.  And the entites then will be names after those roles and not by actors (i.e., you never model the guy typing as an entity). Entities are the roles that the the person takes on as they are actually doing work.

A role distinguishes the different parts played by customers in a shipment. One is the “shipper,” one the “receiver,” one the “payer,” and so on. Because only one
customer can play a given role for a particular cargo, the association becomes a qualified many-to-one instead of many-to-many. Role might be implemented as simply a string, or it could be a class if other behavior is needed.

#### Context Maps
Context map is a map of the system which is showing me the bounded contexts and the relationships that they have between them. And a diagram like this can be extremely useful when you are trying to get a big picture.

#### Entity maps
This diagram will help in the direction of code. The basic problem here is how to put into a concise format the jobs of the individual entities inside the system. Basic idea is CRC card. The basic idea of the CRC card is to try and identify the classes in the system, the responsibilities they have, and the collaborators, who do they talk to? Now, in an entity model, classes are not really going to be classes. They are probably going to be services or something like normal classes, but the responsibilities are particularly important. (Note here we are not intersted in defining methods). Entity map shows us all the entities in the system, and the relationships they have with each other by means of the event system.

![image](https://user-images.githubusercontent.com/10434795/203946112-f85902eb-1d08-441d-983f-30f574758ebe.png)

Context maps are entity map diagrams are not mandatory. They are both useful as system gets larger. For one thing, the entity map diagram can capture information from multiple stories, which you don't see on an individual map, but whether you need it or not going to depend on complexity of the system. But I have found them to be usefful in my own work.
#### Event storming

Above we have looked how DDD systems looks structrually i.e., entities, contexts, roles, ubiquitious langauge, the next question is how do we identify or build these things? How do we design them? How do we do design with business people. How do we analyze the domain/business and develop the code that this modeling the business. There are various methods. Here we see Event storming. Refer to my Event storming.md notes.


#### References

1. Learning Domain Driven Design by Vlad Khononov, Orilley 
2. Domain Driven Design by Eric Evans
3. https://holub.com/blog
