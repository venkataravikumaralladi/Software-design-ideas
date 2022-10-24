EventStorming is a low-tech activity for a group of people to brainstorm and rapidly model a business process. In a sense, EventStorming is a tactical tool for sharing business domain knowledge. An EventStorming session has a scope: the business process that the group is interested in exploring. The participants are exploring the process as a series of domain events, represented by sticky notes, over a timeline. Step by step, the model is enhanced with additional concepts—actors, commands, entities, language,  external systems, and others—until all of its elements tell the story of how the business process works.

Event storming is `collobarative technique` that developer/architect will do with business people in order to come up with a design of a system that models the structure and flow of activities within the business. Note here stories are also important i.e., do the modeling according to the business

`So you sitdown with a story and a bunch of business people and a white board and a bunch of sticky notes and you start modeling.`

![image](https://user-images.githubusercontent.com/10434795/197523522-e3afe931-c7b1-4a5f-b579-b86ad8a6e35e.png)

#### Event storming process

1. First order of business with event storming is business events, and that we write one event per sticky note and arrange the sticky notes from left to right on wihte board. Note these are not programming model level events though this may happen later but these may not happen at beginners. These are business level events.
2. Second order of business is that we will go through events and for each event we will decide what activity (i.e., action, command) has to occur as a result of the event being received.
3. Third order of business is that we decide what aggregate or context or entity is responsible for receiving tthe event and doing the activity
4. Fourth order of business is that we might have optional questions.
5. Fifth order of business that there might be a work product being generated for example a pick list might come out of an order being placed. An invoice, or something like that might be generated by a financial event.
6. Sixth order of business is about adding policies

Once above steps have done we can add little more information. So in case of events we might be interested in what payload the events carry along with them. So the fact that an order has been placed might carry some information with it. For example, the items that comprised the order contains the destination address or something like that. Similarly, the aggregate or the entity, rather, occurs within some context. Sow we are starting to identify both the events and the context within which those events occur.

So to summarize, here we user various colors that you might see in one of the systems. We have events in `orange`, we have commands (actions) in `blue`, aggregates or entities in `yellow`. `green` might identify an actor or some kind of UI activity occuring within the system. And then there are business processes or policies, external system from which events come or to which events are sent, work products, and then finally questions in `red`.

#### Generally used color notations

`Event (Orange)`: An event is something that happens at the business level that customers (end users or domain experts) care about. Rememeber that event is a business level thing that we are implementing the domain. Example of events are order submitted, payment recevied, nightly reconciliation completed. We don't really care who is triggering the event. What we care is the event itself. Also notice that the events are specified in past tense and that's also important. An event is some thing that has happened that will trigger some thing else to happen to next. So putting the events in past tense is a good way to keep them straight, and organize the system. Arrange the events in time line.

`Actions or actvities or commands (blue)`: Here basic idea here is that an event happens and that causes an action to occur. Basic idea is that you start with the events, and then you say okay wehn this event happens what do we want to happen as a result i.e., we take action and then that goes up as a blue note. Blue notes and orange notes generally tend to inter-oven.

`questions (red)`: some times when we are thinking of events and actions we don't know what we have to do. They are the questions that occured in the process of doing the modeling, where the modeling is not complete. As long as red sticky note is there we are not ready to code yet.

`policies (purple)`: policy or business rule that is going to control how the action plays out. So when the event is received, you might then apply a policy and decide what to do next based on what that policy says. So policies are ways to indicate that it is not a smooth linear flow. There are decisions that have to be made here based on some set of business rules.

`aggregates or entities (yellow)`: work product being generated or entity that takes an action or command. For example an invoice might be an product that is generated by a financial event.

`external systems(pink)`: occured from outside world.

#### Output of event storming

When we are done with event storming then we end up with a long piece of paper with a lot of sticky notes on it, but what that shows us is the entire fflow of events through a system as a story is being processed, who is handling all those events, and what context they are part of to name a few.  So this will help developer to program in easy way from the model.

#### Tools for performing event storming

We can use miro tool (https://miro.com/login/)



