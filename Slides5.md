# Design Patterns
## Singleton Design Pattern
* Motivation: there are many objects we need one of. In many cases, instantiating more than one of such objects creates problems
* Ensures that a class has only one instance and provides a global point of access to that instance
* To ensure thread safety, use eager instantiation instead of lazy instantiation
## Command Design Pattern
* Motivation: there are multiple objects to be controlled, each of which need different actions. We need a common interface to request commands to be invoked on varying objects.
* Encapsulates a request as an object, thereby letting you parameterize other objects with different requests, queue or log requests, and support undoable operations
## Adapter Design Pattern
* Motivation: you have legacy code that does not fit the target interface you desire. 
* The Adapter Pattern converts the interface of a class into another interface the clients expect. Adapter lets classes work together that couldn’t otherwise because of incompatible interfaces.
## Façade Pattern
* Motivation: you want to create a simple interface for a family of complex subsystems 
* Provides a unified interface to a set of interfaces in a subsystem. Façade defines a higher-level interface that makes the subsystem easier to use.
