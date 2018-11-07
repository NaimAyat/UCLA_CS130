# Design Patterns
## Info Hiding Recap
* Module: an independent work assignment
* Goal of modularization: parallel development 
## Strategy Design Pattern
* Enables selecting an algorithm at runtime. Instead of implementing a single algorithm directly, code receives run-time instructions as to which in a family of algorithms to use.
* Intent: you have lots of classes / subclasses you want to implement, but some behaviors are not necessary, some are optional, and some are not appropriate
## Observer Design Pattern
* Defines a one-to-many dependency between objects so that when one object changes state, all of its dependents are notified and updated automatically.
* 1 to n relationships
* Publish and subscribe
* Notification / listener-based implementation
* What is easy to change using Observer?
  * Number of observers, adding a new observer to a subject
* What is difficult to do using Observer?
  * Changing internal states of subject and modifying the interface of update
## Mediator Design Pattern
* To centralize complex communications and control between related objects
* With the mediator in place, all objects are all completely decoupled from each other
* Mediator contains all control logic for the entire system
* Mediator benefits: 
  * Increase the reusability of the objects supported by the Mediator by decoupling them from the system
  * Simplifies maintenance of the system by centralizing control logic
  * Simplified and reduces the variety of messages sent between objects in the system
* Mediator drawbacks:
  * Without proper design, the mediator object itself can become overly complex
  * Mediator also exposes a single point of vulnerability and complexity
## Recap
* The Strategy Pattern defines a family of algorithms, and it lets the algorithm vary independently from clients that use it. The choice of the algorithm can be replaced at runtime.
* The Observer Pattern defines a one-to-many dependency between objects so that when one object changes state, all of its dependents are notified and updated automatically.
* The Mediator Pattern encapsulates many to many dependencies between objects. 
