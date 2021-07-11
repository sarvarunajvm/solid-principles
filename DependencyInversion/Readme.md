# Dependency Inversion Principle

<h2 align="center">Simple Definition </h2>

   High-level modules should not depend on low level modules. Both should depend on abstractions. And abstractions should not be depend on details. Details should depend on abstractions.

<h3 align="center">Top Down design</h3>

Extracting all the functionality into standalone classes until all classes follow Single Responsibility principle.And obvious natural outcome is hierarical classes.

<h3 align="center"> Abstractions</h3>

By introducing the abstract layer in your problem some of the dependencies will be inverted.

<h3 align="center"> Open Closed</h3>

As long as abstraction doesn't change middle or a child layer, Parent layer is protected from the changes in core functionalities.And DIP provides protections from changing requirements.

<h3 align="center"> CallBacks</h3>

Will introduce the circular dependencies if it depends on the paren class functionality from the child class and by introducing an abstract layer that can do the task in **async** manner **no chain of dependencies** from service to client.Now service layer is self-contained and can be reused.

<h3 align="center"> Inter dependent</h3>

By implementing the Dependency inversion principle if there is a module is inter dependent for two or more services. We can increase visibility and better accountability.

<h3 align="center">Cost of dependency inversion</h3>

- More effort to implement
- More effort to change
- Increased code complexity due to indirection

> Don not use dependency inversion for the sake of just using it.Beware of overengineering.

<h2 align="center">Summary.</h2>

- [x] DIP advocates for strategic use of abstractions.
- [x] Invert dependencies when benefits outweigh the costs.
- [x] DIP is very powerfull too that requires judicious use.

<h2 align="center">Benefits.</h2>

- [x] DCP Contributes Resuability.
- [x] Increase visibility and better accountability.
- [x] Easier integration.
- [x] Break dependency on the schedule of another component.
- [x] Protection from future changes in requirements.
