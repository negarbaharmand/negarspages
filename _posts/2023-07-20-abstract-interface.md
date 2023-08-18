---
title: TIL Discovering Java's OOP Magic: Abstract and Interface Made Simple
date: 2023-07-20 09:32:00 +0200
categories: [JAVA, OOP]
tags: [java, oop, object] # TAG names should always be lowercase
---

If you've recently stepped into the world of Java programming like me, you're in for a treat. Today, let's tackle abstract classes and interfaces – two things that might sound a bit fancy but are actually quite cool, especially when you're starting out.

## Abstract Classes: Blueprints for Special Things

Imagine you're designing a virtual universe with all sorts of characters, each with their own special features. Abstract classes are like templates for these characters. They're like saying, "Hey, all characters should have some basic stuff, but feel free to add your own unique touches." It's like setting up a framework for making different characters.

For instance:

```java
abstract class Character {
    abstract void makeSound();
    abstract void move();
}

class Knight extends Character {
    void makeSound() {
        System.out.println("Hail, noble friend!");
    }
    // Define how the knight moves
}

class Wizard extends Character {
    void makeSound() {
        System.out.println("Abracadabra!");
    }
    // Define how the wizard moves
}

```

In this example, the '**Character**' abstract class has the basic things every character needs. The '**Knight**' and '**Wizard**' classes then build on this foundation to create their own unique behaviors.

## Interfaces: The Art of Code Contracts

Now, let's explore the fascinating world of interfaces – a concept that might sound complex but is actually quite straightforward. Think of an interface as a contract between different parts of your code. This contract ensures that various classes work together harmoniously, even if they have different implementations.

#### Creating Harmony with Contracts

Imagine you're working on a team project, and everyone needs to follow certain rules to ensure everything runs smoothly. An interface is like a set of agreed-upon rules, or a contract, that different classes promise to adhere to.

Here's a simple way to look at it:

```java
interface Movable {
    void move();
}

class Car implements Movable {
    public void move() {
        System.out.println("The car zooms ahead!");
    }
    // Other car stuff
}

class Bicycle implements Movable {
    public void move() {
        System.out.println("The bicycle pedals away.");
    }
    // Other bicycle stuff
}
```

In this example, the **Movable** interface is the contract. It says, "Any class that wants to be 'movable' must have a **'move'** method." Both the **'Car'** and **'Bicycle'** classes agree to this contract by implementing the move method.
Just as a contract ensures everyone follows the same rules, an interface ensures classes follow the same set of methods. It's a neat way to create order and compatibility in your code. Happy coding, contract maker!
