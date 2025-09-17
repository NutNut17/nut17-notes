---
title: "Java"
description: "Quick note for Java"
summary: ""
date: 2023-09-07T16:04:48+02:00
lastmod: 2023-09-07T16:04:48+02:00
draft: false
weight: 407
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---
{{< threejs-cube >}}

Source: https://webcourse.ncue.edu.tw/Java/index.php

### Basics

Java is a multiplatform object oriented programming language derived from C++. 

```bash
c:\Java> javac ClassName.java   // Compile to bytecode
c:\Java> java ClassName         // Run
```

| . | Description |
| --- | --- |
| JVM (Java Virtual Machine) | The engine that run compiled universal bytecode on the machine |
| JRE (Java Runtime Environment) | JVM + core minimal library to run java programs |
| JDK (Java Development Kit) | JRE + java development tools |
| JAR (Java Archive) | An archive to store java .class and other files |

Syntax

```java
import java.text.*;         // The "*" imports every package in java.text
import java.util.Scanner;
import java.lang.Math;

public class className { // Name of file must be className.java
    public static void main(String args[]) {
        Scanner scn = new Scanner(System.in);
        DecimalFormat f1 = new DecimalFormat("#.00");   // Make an object to specify decimal format
        double base = Double.parseDouble((scn.next()));
        double exponent = Double.parseDouble((scn.next()));
        System.out.println(f1.format(Math.pow(base, exponent)));
        scn.close();

        System.out.println((int) Math.floor(Math.random() * (max - min + 1) + min)); // Random number
    }
}
```

Libraries

| Library | Description |
| --- | --- |
| java.lang.Object | Base of all class |
| java.lang.String | String classes |
| java.util.Date | Date and time classes |
| java.text.Format | Output formatting |
| java.lang.Thread | Multi-thread classes |

Keywords

| Keyword | Description |
| --- | --- |
| public | Other files can access |
| private | Other files can't access |
| protected | Only descendants can access |
| static | Only one global instance |
| final | Can't be modified after initialization, constant |
| new | Create a new instance |
| delete | Delete a class instance by assigning null |
| synchronized | Only one thread can access at a time |

### OOP Concepts

#### Class

Contains member and methods. Details are encapsulated in a class using `private`, `protected`. Use `.this` to refer members of an instance. A class contains constructor and destructor.

Same function name with different parameters is called overloading. Same function name and parameter on inherited class is called overriding.

`abstract` can't be instantiated and is to be overridden by subclass.

#### Inheritance

Child inherit all properties of parent. It is a class that `extends` the parent class. `super()` can used to call a constructor of the parent.

#### Interface

Java can't have multiple inheritance. It can have multiple implementation by `implements`. The interface members was set default as `final` or `abstact` and `public` in the declaration. Interface can be inherited.

#### Polymorphism

Dynamic polymorphism decides which function to call at runtime.

Usually the design will write parent class. If instance of parent is passed to ‘fruit’, it will call the checkout of the overridden class. This is upcasting, a child calls Parent’s method. Downcasting is a type cast from base to derived but is risky.

```java
public class Shop { 
    public int checkout(Fruit fruit, int count) { return fruit.getPrice() * count; } 
    // This two line can be removed, apple and orange is a subclass of Fruit
    // public int checkout(Apple apple, int count) { return apple.getPrice() * count; } 
    // public int checkout(Orange orange, int count) { return orange.getPrice() * count; } 
}

public class Store { 
    public static void main(String[] args) { 
        Payment p1 = new Payment(); 
        p1.checkout(); // upcasting
        payProcess(p1); //downcasting

        Payment p2 = new CreditCardPayment(); 
        p2.checkout(); // upcasting
        payProcess(p2); 
    }

    public static void payProcess(Payment p){ 
        if(p instanceof CreditCardPayment){ 
            ((CreditCardPayment)p).sign();   //downcasting
        }    
    } 
} 
```

#### Packages

> package packageName;
> package packageName.subPackageName;
> import packageName.className;

#### Exception

```java
try{
    throw new exceptionConstructor(); // throws an exception
    method throws exceptionName1, exceptionName2, ... // The method will throw an exception when the method is called
    class className extends exceptionName{} // Inherit an exception
}
catch(exceptionType variableName){ }
finally{ 
    // Code that will always run eventually 
}
```

#### Collection

A data structure classes.

```java
TreeSet<Integer> tset = new TreeSet<Integer>(); // The <Integer> is generic
```

| Data Structure | Description |
| --- | --- |
| Array | Fixed length array |
| ArrayList | Dynamic array |
| LinkedList | Linked list |
| ListIterator | Iterator of LinkedList |
| Vector | Dynamic array |

### Technology

| Library | Description |
| --- | --- |
| AWT (Abstract Windowing Toolkit) | First-gen Window Application GUI |
| Swing | Second-gen Window Application GUI |
| JavaFX | Third-gen Window Application GUI. Modern, CSS, but not bundled with modern JDK |
| JDBC | Java Database Connectivity |
| Java Spring | A framework for building web applications, like Django. Focus on enterprise application |
| Kotlin | Derived from Java |