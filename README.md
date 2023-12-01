# workshopJavaOOP

## What is Java and what is it used for

Java is a programming language and a platform. Java is a high level, robust, object-oriented and secure programming language.

Java was developed by Sun Microsystems (which is now the subsidiary of Oracle) in the year 1995. James Gosling is known as the father of Java. Before Java, its name was Oak. Since Oak was already a registered company, so James Gosling and his team changed the name from Oak to Java.

Modeled after C++, the Java language was designed to be small, simple
and portable across platforms and operating systems, both at the source and at the binary level

*Learn more about Java history at https://www.javatpoint.com/history-of-java*

Java is an object-oriented programming language. Everything in Java is an object. Object-oriented means we organize our software as a combination of different types of objects that incorporate both data and behavior.

Basic concepts of OOPs are:
* Object
* Class
* Inheritance
* Polymorphism
* Encapsulation
* Abstraction

This workshop will not cover all of theses concepts, but feel free to check them out after this workshop !

*Learn more about Java features at : https://www.javatpoint.com/features-of-java*

## Prerequisites

To learn Java, you must have the basic knowledge of C/C++ programming language.

First check if java is installed

```bash
java -version
```

if an error occured, check the `install.md` file

Now that we have the JDK (Java Development Kit; required only for development, coding) and JRE (Java Runtime Environment; required to run Java code and applications) installed, we can now start programming in java.

## Basics of java

First, we will learn how to write a simple java program;
To create a simple Java program, you need to create a class that contains the main method.

### Java Syntax

When we consider a Java program, it can be defined as a collection of objects that communicate via invoking each other's methods.

By convention, a Java file should have the same name as the class. So the file should contain only contain one and only one class.

A class name should start with an upper-cased letter and a method name should start with a lower-cased letter.

Here is a sample of how to print `Hello World` in java

```java
public class MyFirstJavaProgram {
    public static void main(String []args) {
        System.out.println("Hello World");
    }
}
```

You can see that the *MyFirstJavaProgram* class contains a *main* method that calls the *println* method.

### EX1 : Classes

In Java, a class is a fundamental building block of object-oriented programming. It serves as a blueprint or template for creating objects.
Classes are used to define the structure and behavior of objects, allowing you to model real-world entities or abstract concepts in your Java programs.

If you’re used to programming in C, you can think of a class as sort of creating a new composite data type by using `typedef` and `struct`.
Classes, however, can provide much more than just a collection of data,

**Create a Java class `Vehicle`**

Create a java class `Vehicle` that contains the following attributes :

    - Brand
    - Model
    - Year

and the following methods :

    - Accelerate
    - Brake
    - Describe

The Accelerate method will print `I'm putting the pedal to the metal` and the Brake method will print `Woah! Slow down boy!`

The describe method will print the brand, the model and the year of contruction of the Vehicle;

**Java constructors**

A constructor in Java is a special method that is used to initialize objects. The constructor is called when an object of a class is created.
It can be used to set initial values for object attributes.

In our case, we want a constructor that takes 3 parameters and sets all the attributes to the corresponding parameter.

**Create a Java class `JavaProgeam`** 

This class will contain the `main` method.
It will be reused all along this workshop.

For this exercise, you have to create a **new** Vehicle object and call its **Describe** and **Accelerate** methods.

Now, let’s compile the all the source files using the Java compiler ! The java compiler is called `javac`

When the program compiles without errors, you end up with a file called Vehicle.class and a file called JavaProgram.class, in the same directory as your source file.

To run the program, we just have to use `java` followed by the name of the class containing a main method.

Your output should look like this :

```text
I'm a Volkswagen Scirocco made in 2008.
I'm putting the pedal to the metal! (Let's hope the car doesnt explode)
```

To make sure that you understood how to create object, you can do something similar with an `Animal` class.

### EX2 : Inheritance and overriding

Inheritance is one of the most crucial concepts in object-oriented programming, and it has a very direct effect on how you design and write your Java classes.

Inheritance is a powerful mechanism that means when you write a class you only have to specify how that class is different from some other class,

![inheritance](https://github.com/GryphusOneSeven/WorkshopJavaOOP/blob/readme/inheritance.png?raw=true)

Subclasses inherit all the methods and variables from their superclasses.
If the superclass defines behavior that your class needs, you don’t have to redefine it or copy that code from some other class.

**Update the vehicle class**

Add these attributes to the class 

    - Weight
    - Wheels

**Create the class Truck, Car, Motorcycle and make them inherit from the Vehicle Class**

To make a class inherit from another one, we use the keyword `extends`.

**Override each methods of the vehicle class**

Overriding is a feature that allows a subclass to provide a specific implementation of a method that is already provided by one of its super-classes.
When a method in a subclass has the same name, the same parameters or signature, and the same return type as a method in its super-class, then the method in the subclass is said to override the method in the super-class.

We can also call the superclass' method `super()` method and give it the necessary parameters

For each classes' constructor, we can use the superclass' constructor and then set the remaining attributes;

For the `Describe` method, call the superclass method and print the values of the remaining attributes;

Now when we create an instance of all these classes we should have something like this:


```text
--------------------------------
# Exercice 1 output

I'm a Volkswagen Scirocco made in 2008.
I'm putting the pedal to the metal! (Let's hope the car doesnt explode)

--------------------------------

I'm a Ferrari Testarossa made in 1984.
I'm a Car, I weight 1656 kg and I have 4 wheels.

I'm a Scania Frostfire made in 2022.
I'm a Truck, I weight 6000 kg and I have 6 wheels.

I'm a Kawazaki Ninja made in 2013.
I'm a Motorcycle, I weight 170 kg and I have 2 wheels.
```

This type of inheritance is called **Simple Inheritance**, it means that a class can have only one superclass. 

In other object-oriented programming languages, such as C++ and Smalltalk, classes can have
more than one superclass, and they inherit combined variables and methods from all those
classes. This is called multiple inheritance.
Java makes inheritance simpler by being only singly inherited.


### EX3 : Polymorphism / Method Overloading
In Java, Method Overloading allows different methods to have the same name, but different signatures where the signature can differ by the number of parameters or type of parameters, or a mixture of both.

Method overloading in Java is also known as Static Polymorphism, or Early binding.
In Method overloading compared to the parent argument, the child argument will get the highest priority.

In your sub-classes, overload the method **Accelerate** by adding a **String** that correspond to an onomatopoeia of the sound of the vehicle.
You can also do something siliar with the **Brake** method

When you call these methods, you should have an input similar to this :

```text
--------------------------------
# Exercice 1 output

I'm a Volkswagen Scirocco made in 2008.
I'm putting the pedal to the metal! (Let's hope the car doesnt explode)

--------------------------------
# Exercice 2 output

I'm a Ferrari Testarossa made in 1984.
I'm a Car, I weight 1656 kg and I have 4 wheels.

I'm a Scania Frostfire made in 2022.
I'm a Truck, I weight 6000 kg and I have 6 wheels.

I'm a Kawazaki Ninja made in 2013.
I'm a Motorcycle, I weight 170 kg and I have 2 wheels.

--------------------------------

My Ferrari goes like this : VROOOooooooom !

My Scania goes like this : broooooaaaaaAAAAAAARRRR !

My Kawazaki goes like this : vrrrrRRRRRRRrrrrr !

```

### EX4 : Encapsulation

Now you may be asking : "Why do we put 'public' in front of each class method". This is called an **Access modifier**

The access modifiers in Java specifies the accessibility or scope of a method, constructor, or class.
We can change the access level of fields, constructors, methods, and class by applying the access modifier on it. 

There are four types of Java access modifiers:

    - Private: The access level of a private modifier is only within the class. It cannot be accessed from outside the class.
    - Default: The access level of a default modifier is only within the package. It cannot be accessed from outside the package. If you do not specify any access level, it will be the default.
    - Protected: The access level of a protected modifier is within the package and outside the package through child class. If you do not make the child class, it cannot be accessed from outside the package.
    - Public: The access level of a public modifier is everywhere. It can be accessed from within the class, outside the class, within the package and outside the package.
    
There are also non-access modifiers, such as static, abstract, synchronized, native, volatile, transient, etc...
You can check theses out after this workshop

In general, class variables are private and can only be accessed in the class itself.

**You have to modify the accessibility of all variables of each class**

But now you may be asking : "But now, how can I access each data of theses classes?". We can use **getters** and **setters**

The `get` method returns the variable value, and the `set` method sets the value.

Syntax for both is that they start with either get or set, followed by the name of the variable, with the first letter in upper case:

**Create a getter and setter for each variables**
