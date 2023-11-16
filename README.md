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
* Abstraction
* Encapsulation

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

### EX2 : Inheritance

Inheritance is one of the most crucial concepts in object-oriented programming, and it has a very direct effect on how you design and write your Java classes.

Inheritance is a powerful mechanism that means when you write a class you only have to specify how that class is different from some other class,


Subclasses inherit all the methods and variables from their superclasses—that is, in any particular
class, if the superclass defines behavior that your class needs, you don’t have to redefine it or copy
that code from some other class.

