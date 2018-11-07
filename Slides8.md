# Build Management
* A program cannot just be immediately executed after a change
* Intermediate steps are required to build the program
  * Must convert source to object
  * Must link objects together to create program
* Source components are those that are created manually (e.g., Java, Latex)
* Derived components are those created by the computer/compiler (e.g., bytecode, PDF)
## Make 
* One of the most influential and widely used software tools
* MAKE realizes incremental program construction using a system model
* A description of software product that lists individual components, their dependencies, and steps needed for their construction
* MAKE’s system model is specified in a file (usually called Makefile), which consists of a set of rules
* Rules indicate component dependencies and commands needed to build components
### Make Algorithm
* From Makefile and target A0, calculate dependency graph and run depth first search (DFS)
* Question: how does MAKE know if a file has been changed?
  * A: using time stamps from the file system
## Ant
* Like MAKE, ANT works incrementally
  * With every new build, only those targets are realized whose dependencies have changed
* Unlike MAKE, incrementally is not part of the tool
  * Instead it is realized by the individual task implementations
  * E.g., javac task determines dependencies between Java classes automatically and builds just those classes that must be reconstruted
* ANT is a framework; it can easily be extended by additional tasks
  * By subclassing the Task class
* Can configure at runtime (e.g., replace original javac)
