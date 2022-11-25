#### Communication mechanism

Here we will see how entities in DDD will communicate with each other as they're getting work done. There are two ways to do communication. One easy and the other 
one better. 

1.  The easy way to do things is orchestrated or declarative systems.  The basic idea of an orchestrated system is that The basic idea of an orchestrated system is
that one entity tells another entity what to do. This will work ok in monlith kind of applications, but not for micro-service oriented architecutre. This because blue
lines shown below are function calls, where as in micro-service these are network function calls where error handling is different. Declarative systems have a tight 
relationship between services i.e., they are not location independent, one service need to know location, what arguments to pass, what are there types etc to name a few.
That means maintaince is difficult i.e., if you change at one place we need to change at other place.

![image](https://user-images.githubusercontent.com/10434795/203973617-b6397024-8c70-42ca-8e81-98d0f934ec09.png)

2. Cherography/Reactive systems (Also called Pub-Sub model):   What happens if we replace those declarative APIs with generic ones? In other words, now instead of the shopping cart
3.  service telling the billing, and warehouse, and email services what to do, the shopping cart service just announces to the world a new order has been
4.  placed if you're interested in that do something about it. The billing service will be sitting around waiting for that message to be generated.
5.  And it says, oh a new order has been placed I better send the bill. In summary it will publish the event and services which are interested in that event take 
6.  actions. This eliminated tigh coupling. In DDD vast majority of communication between entities are reactive systems. Pub-Sub is usually implemented using messaging system
7.  like kafka, rabbitmq, zeromq etc

![image](https://user-images.githubusercontent.com/10434795/203975121-02c982b2-ec90-42fa-a4ce-10251494d6d0.png)
