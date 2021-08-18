# Software Architecture Cheat Sheet for Daily Usage
### Software Architecture smells and heuristics

Having clean software architecture and staying conform to pre-defined design principles from start of the project is one of the best ways to avoid possible technical debt in the future of that software system. Clean Software Design is a key point for an effective software product.

Let us have a look at some important principles, rules, guidelines that ensure a clean software design:
<br>
<hr>
<br>

_Principles:_

1.  _Loose Coupling —_ if classes use each other, they are coupled together. The less classes are coupled, the easier is to change them.
2.  _High Cohesion —_ degree to which elements of a whole belong together. Components of the class should be highly cohesive.
3.  _Only Local Changes —_ Changes, maintenance, extensions are only local. This leads to no harming whole environment.
4.  _Easy to Remove —_ Software Components should be easily removeable.
5.  _Small Components —_ software system should be only of small components ideally each doing only one task.

<br>

_Class Design:_

1.  _Single Responsibility Principle (SRP) —_ class should do only one task.
2.  _Open Closed Principle (OCP) —_ class should be extended not modified.
3.  _Liskov Substitution Principle (LSP) —_ derived classes must be substitutable for their base classes.
4.  _Dependency Inversion Principle (DIP) —_ depend on abstractions, not on concretions.
5.  _Interface Segregation Principle (ISP) —_ interfaces should be fine-grained
6.  **Classes Should be Small.**
7.  _Do stuff or know others, but not both._

<br>

_Cohesion Principles:_

1.  _Release Reuse Equivalency Principle (RREP) —_ only together releaseable components should be bundled together.
2.  _Common Closure Principle (CCP) —_ classes that change together should be bundled together.
3.  _Common Reuse Principle (CRP) —_ classes that are used together should be bundled together.

<br>

_Coupling Principles:_

1.  _Acyclic Dependencies Principle (ADP) —_ no dependency cycles.
2.  _Stable Dependencies Principle (SDP) —_ depend on direction of stability.
3.  _Stable Abstractions Principle (SAP) —_ the more abstract, the more stable.

<br>

_High-Level Design:_

1.  _Keep Configurable Data at High Levels —_ constants or config datas should be kept in high level.
2.  _Don’t Be Arbitrary —_ have a convention, principle, rule or guidelines and always follow them.
3.  _Prefer Polymorphism To If/Else or Switch/Case._
4.  _Symmetry / Analogy —_ Favour symmetric designs (e.g. Load — Save) and designs that follow analogies (e.g. same design as found in .NET framework).
5.  _Separate Multi-Threading Code —_ isolate multi-thread from rest of the code.
6.  _Code at Wrong Level of Abstraction —_ stay conform to existing abstraction layers.
7.  _Fields Not Defining State —_ fields holding data that does not belong to the state of the instance but are to hold temporary data. Use local variables or extract to a class abstracting the performed action.
8.  _Micro Layers —_ avoid unnecessary design layers.

<br>

_Environment:_

1.  _Project Build Requires Only One Step._
2.  _Executing Tests Requires Only One Step._
3.  _Source Control System —_ Always use a source control system.
4.  _Continuous Integration —_ Assure integrity with Continuous Integration.
5.  _Overridden Safeties —_ Do not override warnings, errors, exception handling

<br>

_Dependencies:_

1.  _Make Logical Dependencies Physical_ — If one module depends upon another, that dependency should be physical not just logical. Don’t make assumptions.
2.  _Singletons / Service Locator_ — Make use of dependency injection.
3.  _Base Classes Depending On Their Derivatives_ — Base classes should work with any derived class.
4.  _Feature Envy_ — The methods of a class should be interested in the variables and functions of the class they belong to, and not the variables and functions of other classes. Using accessors and mutators of some other object to manipulate its data, is envying the scope of the other object (c).
5.  _Artificial Coupling_ — Things that don’t depend upon each other should not be artificially coupled.
6.  _Hidden Temporal Coupling_ — If the order of some method calls is important, then make sure that they cannot be called in the wrong order.
7.  _Transitive Navigation_ — (Law of Demeter), writing shy code. A module should know only its direct dependencies.

<br>

