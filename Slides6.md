# Design Patterns
## Template Method
* Motivation: varying objects want to do similar things but slightly different ways
* Defines the skeleton of an algorithm in a method, deferring some steps to subclasses. Template Method lets subclasses redefine certain steps of an algorithm without changing the algorithm’s structure.
## State Method
* Motivation: You’d like to code a complex state transition. You’d like to not forget “defining state transitions” for each state and check this at compile time! 
* Allows an object to alter its behavior when its internal state changes. The object will appear to change its class
## Flyweight Pattern
* Motivation: save resources by sharing objects when one instance can be used to provide many virtual instances
* One instance of a class can be reused to provide many virtual instances.
## Difference Between Observer and Mediator
* Observer 1:n relationship between subject and observers. 
* Mediator abstracts n:n relationship among multiple objects.
* Every object only knows about Mediator and trusts Mediator to call other objects that I want to communicate. 
* Easy to add a new observer in Observer. 
