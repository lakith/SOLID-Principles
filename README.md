# SOLID-Principles
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
![Liskov Substitution Principle](https://1.bp.blogspot.com/-Krp8u7RTb8I/WFqA6Y7kfNI/AAAAAAAACyE/tm3jMnQE_1gnWt9Rwwf95iKGBXcE4QEkACLcB/s1600/LSP_WithText-mallard-duck.jpg)

