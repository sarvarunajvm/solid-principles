
# Open Closed Principle

   <h2 align="center">
	Simple Definition : 
   </h2>

Software entities should be **open for extension**, but **closed for modification.** Also refers as polymorphism as we dig deeper refer the **Protected variation: The Importance of being closed**.

> OCP definition looks self-contradictory on the first sight.

### Open for extension ?
1. Inheritance?
2. Polymorphism?
3. Adding more code to a class 
  > All the above sounds reasonable to the term open for extension

### Closed for modification ?
1. How do i Refactor my code?
2. How do i fix the bugs?
3. If the requirements changes how do i acheive without modification?
4. If no class in the codebase changes, how do i add new functionalities? 
> All the above are very confusing to the reality we are facing day-to-day.

   <h2 align="center">
	The original definition.
   </h2>

1. No implementation changes after classes released to clients.
2. Should be possible to extend all the classes.

> Design and document for inheritance or else prohibit it.

### Actual meaning of OPEN 
   
A class is said to be open if it is still **available for extension**. 

>ie., Class should be possible to expand its set of operations or add fields to its data structures.

### Actual meaning of CLOSED
 
A class is said to be closed if it is **available for use by other modules**. This assumes that the module has been given a well-defined, stable description *(its interface in the sense of information hiding **abstraction**)*. 

>ie., At the implementation level, closure for class also implies that you may compile it, perhaps store it in a library, and make it available for other(its clients) to use.

   <h2 align="center">
	Current context.
   </h2>
   
#### How is it possible that the behaviours of a module can be modified without changing the source code ?
Abstraction is the answer. In Object oriented programming language(OOPL), It is possible to create abstractions that are fixed and yet represent and unbounded group of possible behaviours, The abstractions are abstarct base classes, and the unbounded group of possible behaviours are represented by all the possible derivative classes.

Its poossible for a class to manipulate an abstraction. Such classes can be closed for modification, Since its depends on an abstraction that is fixed. Yet the behaviour of that classes can be extended by creating new derivatives of the abstraction.

> Depend on stable abstractions and modify system's behaviour by providing different realizations.
     
   <h2 align="center">
	Cost of abstractions.
   </h2>
   
1. We need to write additional code.
2. Abstraction make your code more complex.
3. Wrong abstractions can be extremely hard to fix later.

> Beware of complexity and use abstractions only when if the situation are unavoidable. because the fact that something can change doesn't imply that it will change, or that it will change according to your predictions.

   <h2 align="center">
	OCP Application framework.
   </h2>
   
1. Is the anticipated change related to intrinsic instability of the business requirements?.
2. What kind of changes usually happen on projects like this one?
3. If the potential change doesn't correspond to 1 or 2 above, dont apply OCP.
4. When requirements change, identify opportunities for extraction of meaningful abstractions and then refactor accordingly.

>Like other principles this principle can also lead to over-engineering.

   <h2 align="center">
	OCP Limitations.
   </h2>
   
1. Not applicable to all classes in your application.
2. Can't protect from all possible changes.
3. Wrong abstractions can be very hard to fix.

   <h2 align="center">
	Things to look Before apply.
   </h2>
   
1. Apply OCP initially only when you're certain about the nature of future changes.
2. Monitor changes in requirements and extract useful abstractions as you go.

   <h2 align="center">
	Summary.
   </h2>

Protect your existing code from a subset of potential future changes that you can predict.

- [x] Entities should be **open for extension**, but **closed for modification.**
- [x] Abstraction is the answer.
- [x] Abstraction make your code more complex.
- [x] Wrong abstractions can be very hard to fix.
- [x] Monitor changes in requirements and extract useful abstractions as you go.

   <h2 align="center">
	Benefits.
   </h2>
- [x] Proper utilization of OCP allows us to provide additional business value quickly and safely.