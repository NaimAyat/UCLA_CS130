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
## JAVADOC 
* Extracts documentation from special comments and converts it into hypertext (HTML)
* Documentation becomes a part of the system and can be maintained and constructed with automated tools
## Recap
* The aim of automatic program construction is to create all derived components from a number of source components.
* If a component has changed, all the components derived from it must be rebuilt.
* MAKE is a tool for building programs, during the course of which existing derived files are reused as much as possible.
* ANT allows specific extensions by the user as well as third parties. ANT is more task oriented. 
* If the documentation becomes part of the source text, it can be maintained and edited with tools.
* It is easier to keep the documentation synced with source code. 
