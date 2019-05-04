# SOLID-Principles

![Single Responsibility Principle](https://agilecoach2016.files.wordpress.com/2017/12/solid-small.jpg?w=400)
<br/>
<br/>

### Single Responsibility Principle.

In this context, a responsibility is considered to be one reason to change. This principle states that if we have 2 reasons to change for a class, we have to split the functionality in two classes. Each class will handle only one responsibility and if in the future we need to make one change we are going to make it in the class which handles it. When we need to make a change in a class having more responsibilities the change might affect the other functionality related to the other responsibility of the class

![Single Responsibility Principle](https://exceptionnotfound.net/content/images/2015/03/singleresponsibilityprinciple.jpg)

<br/>
<br/>

### Open Close Principle.
The general idea of this principle is great. It tells you to write your code so that you will be able to add new functionality without changing the existing code. That prevents situations in which a change to one of your classes also requires you to adapt all depending classes. Unfortunately, Bertrand Mayer proposes to use inheritance to achieve this goal.

![Open Close Principle](https://res.cloudinary.com/practicaldev/image/fetch/s--XI1FFTvi--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/http://d33wubrfki0l68.cloudfront.net/d1820d6c153e116bb211cc3e4499de8a8a40cf8e/b43f4/assets/images/open_closed_1.png)
That basically means that you should write your modules in a way that wouldn't require you to modify it's code in order to extend it's behavior
<br/>
<br/>

### Liskov Substitution Principle.
In mathematics, a Square is a Rectangle. Indeed it is a specialization of a rectangle. The "is a" makes you want to model this with inheritance. However if in code you made Square derive from Rectangle, then a Square should be usable anywhere you expect a Rectangle. This makes for some strange behavior.
<br/>
Imagine you had SetWidth and SetHeight methods on your Rectangle base class; this seems perfectly logical. However if your Rectangle reference pointed to a Square, then SetWidth and SetHeight doesn't make sense because setting one would change the other to match it. In this case Square fails the Liskov Substitution Test with Rectangle and the abstraction of having Square inherit from Rectangle is a bad one.
<br/>
![Liskov Substitution Principle](https://1.bp.blogspot.com/-Krp8u7RTb8I/WFqA6Y7kfNI/AAAAAAAACyE/tm3jMnQE_1gnWt9Rwwf95iKGBXcE4QEkACLcB/s1600/LSP_WithText-mallard-duck.jpg)

### Interface segregation principle.
Similar to the Single Responsibility Principle, the goal of the Interface Segregation Principle is to reduce the side effects and frequency of required changes by splitting the software into multiple, independent parts.
<br/>
As Per the We introduce a Interface to perform document related works. First machine, interface violates the interface segregation principle, because in this principle we must not include all the funcinalities in a single interface. according to the code, if we want a printer that only perform the printing, if we use the first interface, we should implement other two functinalities inside that code, and its not necessory. Because it does not perform scanning or faxing. In a better design we should split these functionalities into diffrent interfaces. 

![interface segregation principle](https://4.bp.blogspot.com/-z9uPLDKMN2o/WmnophiErMI/AAAAAAAAKQ8/KyCrLwN20Iorkw73TNJbzog0kJbHWDZ_gCLcBGAs/s400/OOP%2B-%2BInterface%2BSegregation%2BPrinciple.jpg)

 ### Dependency Inversion Principle.

The general idea of this principle is as simple as it is important: High-level modules, which provide complex logic, should be easily reusable and unaffected by changes in low-level modules, which provide utility features. To achieve that, you need to introduce an abstraction that decouples the high-level and low-level modules from each other.
<br/>
<br/>
Based on this idea, Robert C. Martin’s definition of the Dependency Inversion Principle consists of two parts:
<br/>
* High-level modules should not depend on low-level modules.
* Both should depend on abstractions.
<br/>
Abstractions should not depend on details. Details should depend on abstractions.
An important detail of this definition is, that high-level and low-level modules depend on the abstraction. The design principle does not just change the direction of the dependency, as you might have expected when you read its name for the first time. It splits the dependency between the high-level and low-level modules by introducing an abstraction between them. So in the end, you get two dependencies:
<br/>
* The high-level module depends on the abstraction.<br/>
* The low-level depends on the same abstraction.
![Dependency Inversion Principle](https://i0.wp.com/blogs.innovationm.com/wp-content/uploads/2017/11/DependencyInversionPrinciple.jpg?fit=750%2C600)

## Summery

#### Single Responsibility Principle.
* A Class Should only have One Reason TO Change
* Separation Of Concerns - Different classes handling different, independent tasks/problems


#### Open-Closed Principle.
* Classes should be open for extension but closed for modification.


#### Liskov Substitution Principle. 
* You Should be able to substitute a base type for a subtype.

#### Interface Segregation Principle.
* Don't Put too much into an interface, Split into Separate Interfaces.
* YAGNI - You Ain't Goning to need it.

#### Dependancy Inversion Principle. 
* High-level modules should not depend upon low-level ones; Use Abstractions.

