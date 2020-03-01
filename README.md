Polymorphism Definition
Allows us to perform a single action in different ways.

Two types of Polymorphism

1) Compile time -  This type of polymorphism is achieved by method overloading or operator overloading.
 
 a) Method Overloading - When there are multiple functions with same name but different parameters then these functions are said to be overloaded. 
  b) Operator Overloading: Java also provide option to overload operators. For example, we can make the operator (‘+’) for string class to concatenate two strings.

2) Runtime Polymorphism -  It is a process in which a function call to the overridden method is resolved at Runtime. This type of polymorphism is achieved by Method Overriding.

  a) Method overriding, on the other hand, occurs when a derived class has a definition for one of the member functions of the base class. That base function is said to be overridden.


Polymorphism Can be achieved by
1) Overloading
2) Overriding

Example
Real life example of polymorphism: A person at the same time can have different characteristic. Like a man at the same time is a father, a husband, an employee. So the same person posses different behaviour in different situations. This is called polymorphism.

Usages and Advantages of Polymorphism
1) Method overloading allows methods that perform similar or closely related functions to be accessed through a common name. For example, a program performs operations on an array of numbers which can be int, float, or double type. Method overloading allows you to define three methods with the same name and different types of parameters to handle the array of operations.

2) Method overloading can be implemented on constructors allowing different ways to initialize objects of a class. This enables you to define multiple constructors for handling different types of initializations.

3) Method overriding allows a sub class to use all the general definitions that a super class provides and add specialized definitions through overridden methods.

4) Method overriding works together with inheritance to enable code reuse of existing classes without the need for re-compilation.

****************************************************************************************************************************************
Inheritance in Java
inheritance represents a IS-A relationship. This object is a type of that object.

definition

1) Inheritance in Java is a mechanism in which one class acquires all the properties and behaviors of a parent class.
2) The idea behind inheritance in Java is that you can create new classes that are built upon existing classes. When you inherit from an existing class, you can reuse methods and fields of the parent class. Moreover, you can add new methods and fields in your current class also.
3) Inheritance represents the IS-A relationship which is also known as a parent-child relationship.
4) It is the mechanism in java by which one class is allow to inherit the features(fields and methods) of another class.
6) Inheritance is a mechanism wherein a new class is derived from an existing class. In Java, classes may inherit or acquire the properties and methods of other classes. A class derived from another class is called a subclass, whereas the class from which a subclass is derived is called a superclass. A subclass can have only one superclass, whereas a superclass may have one or more subclasses.
7) The process by which one class acquires the properties(data members) and functionalities(methods) of another class is called inheritance. The aim of inheritance is to provide the reusability of code so that a class has to write only the unique features and rest of the common properties and functionalities can be extended from the another class.

Why use inheritance in java
1) For Method Overriding (so runtime polymorphism can be achieved).
2) For Code Reusability.

Types of Inheritance in Java
1) Single Inheritance
2) Multilevel Inheritance
3) Hierarchical Inheritance
4) Multiple Inheritance  (Through Interfaces) -  In Multiple inheritance ,one class can have more than one superclass and inherit features from all parent classes. 
Please note that Java does not support multiple inheritance with classes. In java, we can achieve multiple inheritance only through Interfaces.
5) Hybrid Inheritance(Through Interfaces) - only with Interfaces


Super/Constructor keyword -
1) The keyword super can be used to access any data member or methods of the parent class.
2) Super keyword can be used at variable, method and constructor level.
3) Call to super() must be the first statement in subclass Class constructor.
4) If a constructor does not explicitly invoke a superclass constructor, the Java compiler automatically inserts a call to the no-argument constructor of the superclass. If the superclass does not have a no-argument constructor, you will get a compile-time error. Object does have such a constructor, so if Object is the only superclass, there is no problem.
5) If a subclass constructor invokes a constructor of its superclass, either explicitly or implicitly, you might think that a whole chain of constructors called, all the way back to the constructor of Object. This, in fact, is the case. It is called constructor chaining..

How it is acvhied
using extends keyword

Java Object Creation of Inherited Class
1) One sub class object is only created
2) super.getClass().getName() return sub class name

https://www.geeksforgeeks.org/gfact-52-java-object-creation-of-inherited-classes/

Why multiple inheritance is not supported in java?
1) To reduce the complexity and simplify the language, multiple inheritance is not supported in java.
2) There will be ambiguity

Class Vs object
Class - It is a template or blueprint from which objects are created.

****************************************************************************************************************************************


Encapsulation in Java
1)	Is a mechanism of wrapping the data (variables) and code acting on the data (methods) together as a single unit. 
2)	In encapsulation, the variables of a class will be hidden from other classes, and can be accessed only through the methods of their current class. Therefore, it is also known as data hiding.

To achieve encapsulation in Java −

Declare the variables of a class as private.

Provide public setter and getter methods to modify and view the variables values.


Advantage of Encapsulation in Java

a) By providing only a setter or getter method, you can make the class read-only or write-only. In other words, you can skip the getter or setter methods.

b) It(Setters) provides you the control over the data. Suppose you want to set the value of id which should be greater than 100 only, you can write the logic inside the setter method. You can write the logic not to store the negative numbers in the setter methods.

c) It is a way to achieve data hiding in Java because other class will not be able to access the data through the private data members.


****************************************************************************************************************************************
Abstraction in Java

Definition:

1) Abstraction is selecting data from a larger pool to show only the relevant details and hides the irrelevant details.
2) abstraction is a process of hiding the implementation details from the user, only the functionality will be provided to the user. In other words, the user will have the information on what the object does instead of how it does it.

Why:
It helps to reduce programming complexity and effort.

How to achive
1)	Abstract classes and 
2)	interfaces.

Example : Mobile or TV
Ex: A car is viewed as a car rather than its individual components. Data Abstraction may also be defined as the process of identifying only the required characteristics of an object ignoring the irrelevant details.


****************************************************************************************************************************************

Abstraction vs. Encapsulation
Often encapsulation is misunderstood with Abstraction. Lets study-

a) Encapsulation is more about "How" to achieve a functionality
b) Abstraction is more about "What" a class can do.

Example :
A simple example to understand this difference is a mobile phone. Where the complex logic in the circuit board is encapsulated in a touch screen, and the interface is provided to abstract it out.

****************************************************************************************************************************************

Aggregation in java
https://beginnersbook.com/2013/05/association/
Aggregation represents Has-A relationship (Student Has-A Address).

Aggregation is a special form of association. It is a relationship between two classes like association, however its a directional association, which means it is strictly a one way association. It represents a HAS-A relationship.


Example :
For example consider two classes Student class and Address class. Every student has an address so the relationship between student and address is a Has-A relationship. But if you consider its vice versa then it would not make any sense as an Address doesn’t need to have a Student necessarily.

Why we need Aggregation?

To maintain code re-usability. To understand this lets take the same example again. Suppose there are two other classes College and Staff along with above two classes Student and Address. In order to maintain Student’s address, College Address and Staff’s address we don’t need to use the same code again and again. We just have to use the reference of Address class while defining each of these classes like:

Student Has-A Address (Has-a relationship between student and address)
College Has-A Address (Has-a relationship between college and address)
Staff Has-A Address (Has-a relationship between staff and address)
****************************************************************************************************************************************

What is Association in java?

Association establishes relationship between two separate classes through their objects. The relationship can be one to one, One to many, many to one and many to many.

Both the classes represent two separate entities.
***************************************************************************************************************************************



**Why do we use interface ?**

It is used to achieve total abstraction.
Since java does not support multiple inheritance in case of class, but by using interface it can achieve multiple inheritance .
It is also used to achieve loose coupling.
Interfaces are used to implement abstraction. So the question arises why use interfaces when we have abstract classes?
The reason is, abstract classes may contain non-final variables, whereas variables in interface are final, public and static.



**Abstract class vs Interface**

*Type of methods: *
Interface can have only abstract methods. Abstract class can have abstract and non-abstract methods. From Java 8, it can have default and static methods also.

Final Variables: 
Variables declared in a Java interface are by default final. An abstract class may contain non-final variables.
Type of variables: 
Abstract class can have final, non-final, static and non-static variables. Interface has only static and final variables.

Implementation: 
Abstract class can provide the implementation of interface. Interface can’t provide the implementation of abstract class.

Inheritance vs Abstraction: 
A Java interface can be implemented using keyword “implements” and abstract class can be extended using keyword “extends”.

Multiple implementation: 
An interface can extend another Java interface only, an abstract class can extend another Java class and implement multiple Java interfaces.

Accessibility of Data Members: 
Members of a Java interface are public by default. A Java abstract class can have class members like private, protected, etc.





https://www.geeksforgeeks.org/difference-between-abstract-class-and-interface-in-java/

https://dzone.com/articles/when-to-use-abstract-class-and-intreface

https://www.guru99.com/interface-vs-abstract-class-java.html





