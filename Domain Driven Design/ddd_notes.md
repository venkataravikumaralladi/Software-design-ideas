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

4. `Ubiquitous language`: The idea of the ubiquitious language is that within a given context, the people who are working in that context use a language of their own and the language of one context is difffernt from the language in other contexts. For example in book store context when we are talking about book, what you care about are things that are relevant to the responsibility of the people who are working in that context, in other words, they are relevant to sales. So if you are thinking about the book, the language of books is going to talk about things like authors, reviews, readability and length and stfff that a reader would be interested in when you are trying to sell a book to them. On the ware house context side, the language, the definition of a book is different because you don't really want to sell it anymore, here language of books involves weight, size, things that are of interest to people that are taking books and putting them into boxes and sending them off to people. So this differences occur not just noun level but also at verb level, in other words, the things that you do do books is different, depending on which context you are in and those things are captured in the language, So on the sales side you sell books obviously or you shelf books or you organize books. Over on ware-house side, you pick books off the shelves and you box the books and soon and so forth. The languages are different.  Formalizing ubiquitious languages is an important part of DDD, `the basic idea here is that language itself will be reflected in the code`

  So the words that are used to describe a book will be different with in the ware house context than they are with in the store context. So as a consequence when     you implement , the namess of things will be different is that ware-house kinds of names will be used on the ware house side and book kinds of names will be used   on book store. 

  So this is ubiquitious langauge that reflects at every level. `It is the lanaugage that you programmer or architect will be using as you talk about the problems you are solving.` It is langauge that is reflected in the code itself, in that that will provide names for things that appear in the code. And it's a language that is going to be used at the domain level itself in order to describe the work that's going on. So it is ubiquitious, but it is ubiquitious within a specific context.

One the great tests to see whether something belongs in a context or not is to look at the way that you describe that something and see which langauge is most appropriate for that someghing.

5. `Roles`: 



#### References

1. Learning Domain Driven Design by Vlad Khononov, Orilley 
2. Domain Driven Design by Eric Evans
