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
We will also use this knowledge of the business domain to drive high-level design decisions:decomposing systems into components and defining their integration patterns. The `strategic` aspect of DDD deals with answering the questions of `“what?”` and `“why?”` —what software we are building and why we are building it. 

Domain-driven design’s tactical tools address a different aspect of communication issues. DDD’s `tactical patterns` allow us to write code in a way that reflects
the business domain, addresses its goals, and speaks the language of the business. The tactical part is all about the “how”—how each component is `implemented`.

#### DDD structures and terminology

When you are thinking about DDD, it is about organizing code along certain well-defined boundaries.

1. `Bounded contexts`: It is a natural division within a business. Example: context is book store (purpose is deal with the sales), and there is another context in order for book store to work is for example another context is "book ware house" (purpose is deal with delivering). This is important i.e., thinking in terms of purpose and responsbilities will help us to keep contexts seperate from each other i.e., think in terms of what are the responsbilities of the people working in that context. To communicate between contexts we create a seperate module which talks to outside world of context.

2. `Entity`: An entity is an individual with in a given context. So entity is much like an object/class in object oriented world, it has one job and does one thing and does that one thing in that specific context.

3. `Aggregate`: An aggregate is a collection of entiteis you talk to through a single portal.

4. `Ubiquitous language`: 



#### References

1. Learning Domain Driven Design by Vlad Khononov, Orilley 
2. Domain Driven Design by Eric Evans
