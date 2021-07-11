# Liskov Substitution Principle

            This is the most complicated principle in the SOLID principle. 
            And the only principle named after a real person(Barbara Liskov). 

<h2 align="center">Simple Definition : </h2>

LSP is necessary where some code thinks it is calling the methods of a type `T`, and may unknowingly call the methods of a type `S`, where `S extends T` (i.e. `S` inherits, derives from, or is a subtype of, the supertype `T`).

## Why and how LSP?

1. Are there specific criteria for replaceability of supertypes by subtypes?
2. Is there a framework we can use to identity LSP voilations ahead ?
3. What so important in LSP?

### SubType?

   Subclass or realization which can be substituted for the type it extends or implements.

<h2 align="center">Quote from Liskov's 1988 paper.</h2>

Absractions can be uses to encapsulate potential modifications. i.e., Suppose we want a program to run on different machines. We can accomplish this by inventing abstractions that hide the differences between machines so that to move the program to a different machine only those abstractions need be reimplemented. A good design principle is to think about expected modifications and organize the design by using abstractions that encapsulate the changes.

> Above quote meaning is simply say this is also a variant of Open Closed Principle.

<h2 align="center">LSP Rules.</h2>

1. Method Signature Rule.
     - Contravariance of arguments(In Parameters).
     - Covariance of result(out return type).
     - Exception rule.
2. Method Rule.
   - Pre-Condition rule.
   - Post-Condition rule.  
3. Class Property Invariant Rule.
4. Class Property Constraint Rule.

<h2 align="center">Method Signature Rule.</h2>

### Contravariance of arguments

If subclass implements a method from its superclass, then the number of arguments should be the same.
   The type of each argument in subclass method should be the supertype of the type of the respective argument in superclass method.

   > Equal number of arguments in overridden methods. And don't make subclass methods arguments more specific!
  
### Covariance of result

  Either both superclass and subclass methods return result, or neither does. If there is a result, then the type of the result in the subclass is a subtype of the type of the result in the superclass.

   > Overridden method returns a result if and only if the parent method does too. And don't make subclass methods return types more general!

### Exception rule

  Exceptions thrown by a method in the subclass should be contained in the set of exceptions thrown by the respective method in the superclass.

#### Checked vs unchecked exceptions

Exception rule is enforced by the compiler for "checked" exceptions.
         The compiler doesn't check "unchecked" exceptions

   > If an exception isn't a subtype of exception in supertype, there is a problem with the exception

<h2 align="center">Method Rule.</h2>

### Pre-Condition rule

   An assertion about the state of the system before the method is called.Pre-conditions required by methods of a subclass must not be stronger than the pre-conditions required by the methods of a superclass.

   >A subclass should be able to operate in all states that a superclass can operate in.

### Post-Condition rule
  
  An assertion about the state of the system affter the method execution completes. Post conditions guaranteed by methods of a subclass must not be weaker than the post-conditions guaranteed by the methods os a superclass.
  
>Client shouldn't be suprised by the results of invocation of methods of a subclass.

<h2 align="center">Class Property Invariant Rule</h2>

   An assertion about a specific class property which is always true. Invariants guaranteed by a subclass must include all invariants guaranteed by a superclass.

> Independent of the history, Relatively easy to identify and reason about

<h2 align="center">Class Property Constraint Rule</h2>

   An assertion about how class property evolves over time.Constraint enforeced by a subclass must include all the constraint enforced by a superclass. Constraint express dynamic properties of a class.

> Once state is reached, the class should remain in that state forever.

<h2 align="center">Summary.</h2>

Protect your existing code from a subset of potential future changes that you can predict.

- [x] Subclass or realization which can be substituted for the type it extends or implements.
- [x] Follow the method rule and class rule to identify the LSP.
- [x] Design and document for LSP, is crucially important for type hierarchies and libraries.

<h2 align="center">Benefits.</h2>

- [x] Code re-usability.
- [x] Reduced coupling.
- [x] Easier maintenance.
