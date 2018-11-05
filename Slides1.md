# UML: Unified Modeling Language
## Behavioral Modeling with UML
* Behavioral diagrams are used to capture the dynamic execution of a system
  * Use case diagrams
  * Interaction diagrams
    * Sequence diagrams
  * State diagrams
  * Activity diagrams
### Use Case Diagrams
* Capture the requirements of a system from the user's perspective
* Graph shows:
  * Actors - stick figures
    * A role that a user takes when invoking a use case
    * A single user may be represented by multiple actors
  * Use cases - ovals
  * Edges from actor to use case showing that the actor is involved in the use case
* Use cases have relationships to each other
  * Inclusion
  * Generalization / specialization
  * Extension expresses an exceptional variation of a use case
#### Use Case Generalization
* Like a class generalization, a specialized use case can replace or enhance the behavior
* Ex: `Synchronize Wirelessly` and `Synchronize Serially` point to `Synchronize Data`
#### Use Case Inclusion
* A use case can include the behavior of another use case
* Ex: `Purchase Item` and `Track Packages` are included in `Login`
#### Use Case Extension
* Use case extension encapsulates a distinct flow of events that are not considered part of the normal or basic flow
* Ex: `Log Debugging Info` extends `Purchase Item`
### State Diagrams
* A state represents a condition of a modeled entity for which some action is performed, some stimulus is received, or some condition is met elsewhere in the system
* An action is an atomic execution
* An activity is a more complex collection of behavior that may run for a long duration
* A transition between two states is represented as an arc from one state to the other
  * Can be labeled with triggers, guard conditions, actions, and the event or action that creates the entity
* The initial state is a solid black circle
### Class Diagrams
* Models static relationships between the components of a system
* Classes represent concepts within a system, typically named using nouns
* A single class represents one or more objects in the system at runtime
* The multiplicity of a class is specified by a number in the upper right corner of the component
  * Usually omitted and assumed to be more than 1
  * Specifying a multiplicity of 1 indicates the class should be a singleton
* Each box is a class
  * Name of class
  * List fields (AKA attributes)
    * Visibility, type, multiplicity
  * List methods (AKA functions)
#### Class Relationships
* Attribures can also be represented in class relationship notation
* A line is drawn between the owning class and the target attribute's class
* Edges show relationships between classes
  * Dependency
  * Association
  * Aggregation
  * Composition
  * Generalization
  * Realization
##### Dependency
* Weakest realationship
* Depicted by a dotted arrow from A to B when class A uses class B
* Ex: `Train` uses `ButtonPressedEvent`
##### Association
* Slightly stronger relationship
* Depicted by number labels and a solid arrow to indicate multiplicity when class A has a class B
* Ex. `Train` has a `Button`
##### Aggregation
* Strong association
* Class A owns class B
* Depicted same as association, but arrow starts from empty diamond
* Lifetime association (aggregation) vs. long-term association 
##### Composition
* Strongest relationship
* Class A is made up of class B
* Depicted same as aggregation, but arrow starts from filled diamond
##### Generalization
* Shows inheritance
* Subclass B has an is a relationship with superclass A, or superclass A is a generalization of subclass B
* Same as `extends` in java
* Depicted by filled arrow from subclass to superclass
* Ex. `EmergencyButton` and `RequestButton` inheret from `Button`
##### Realization
* Shows subtyping
* Class A implements interface B
* Depicted by filled arrow with dotted line
#### Operations in Class Diagrams
* Visibility
  * Public + 
  * Private =
  * Protected #
  * Package ~
* Parameter list
  * Direction (in/out)
  * Name
  * Type
  * Multiplicity
* Polymorphism
* Abstract operations (italics)
#### Constraints on Operations
* Pre condition: express what the state of the system must be before the associated operation can be invoked
* Post condition: express what the state of the system will be after the operation completes
* Body condition (invariants):  express constraints on the method. It must be overridden by subclasses
#### Template Class
* Templates (generic types) allow a developer to design a class without specifying the exact types on which the class operates
### Sequence Diagrams
* Show a time-based view of messages between objects
* Think of as a table: 
  * Columns are classes and/or actors
  * Rows are time steps
  * Entries shwo control/data flow (method invocations, important state changes)
* Each object has a dashed lifeline running vertically down the diagram
  * Objects destroyed during the time covered by the sequence are not usually drawn beyond the message that killed the object
#### Sequence Diagram Frames
* `alt`: Alternative fragment for mutual exclusion logic expressed in the guards
* `loop`: Loop fragment while guard is true. Can also write loop(n) to indicate looping n times. There is discussion to extend to include a FOR loop (e.g., loop (i, 1, 10)
* `opt`: Optional fragment that exceeds if guard is true
* `par`: Parallel fragments that execute in parallel
* `region`: Critical region within which only one thread can run
