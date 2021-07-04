# Single Responsibility Principle

   <h2 align="center">
	Simple Definition : 
   </h2>

This is the most important principle in the Object-Oriented-Design. Each Class in our system should have only one responsibilty    

   <h2 align="center">
	What constitute responsibilty   ?
   </h2>

Impossbile to reason about since there is no precise definition of "Responsibility".
 i.e, Different persons have different opinions and prespective about the term responsibility.
 Therefore we cannot determine this principle based on the responsiblility. 

   <h2 align="center">
	Definition through conjuction "AND"
   </h2>
   
   Other way to determine the principle we will be able to describe what each class does without saying "AND". Its not possible for us to explain the functionality without saying "AND" . Therefore we need to find the better definition to explain the SRP.
     
   <h2 align="center">
	Practical definition through change.
   </h2>
   
  Each class should have only one reason to change.
1. Class follows SRP = Can't think of more than one reason for a class to change.
2. Enables collaboration 
3. Questions about changes can be escalated.

So in simple words **responsibility = reason to change**.

   <h2 align="center">
	Problem with voilations of this principle?
   </h2>
SRP voilations lead to excessive coupling. 

1.  Involvement of different stackholders in class-level functionality is an indication of "SRP" voilation.

   <h2 align="center">
	How to deal with this problem?
   </h2>
We can extract individual responsibilities into standalone classes. Be practical when you think about the future impacts and beware of over-engineering and stay pragmatic.

1. Analyse the feature and find out that contained too much functionality
2. Analyse the flow and indentify the SRP voilations
3. Extract individual responsibilities(**reason to change**) into standalone classes. 
4. Lastly identify the responsibility of feature itself as **Final State Machine** 
5. Analyse and make sure before you write code.
   
   <h2 align="center">
	Single Responsibility and Reusability.
   </h2>
   Simple solution is to break your feature into smaller classes for easier reuse.

   <h2 align="center">
	Summary.
   </h2>
- [x] No clear definition of responsibility
- [x] Each class should have only one reason to change (**Practical definition**).
- [x] List all your feature requirement.
- [x] Analyse each item in the list to identify potential reasons to change.
- [x] Extract functionalities that change due to different reasons into standalone classes.

   <h2 align="center">
	Benefits.
   </h2>
- [x] Smaller, narrowly focused components.
- [x] Encapsulation of the most probable changes within specific components.
- [x] Better implementation decisions
- [x] Simpler reuse of existing functionality
- [x] More flexibility of the codebase as a whole.