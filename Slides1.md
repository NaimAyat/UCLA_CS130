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
