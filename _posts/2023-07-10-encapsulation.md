---
title: "TIL Encapsulation: Your Code's Protective Capsule"
date: 2023-07-10 10:32:00 +0200
categories: [JAVA, OOP]
tags: [java, oop, object] # TAG names should always be lowercase
---

![Capsule](/assets/images/capsule.jpg)

Let's talk about a super useful concept in Java programming: encapsulation. It might sound fancy, but it's like giving your code a protective capsule, just like the one around medicine.

Imagine you have a special capsule that holds a secret gem. You don't want anyone touching or changing the gem, right? In Java, you can achieve this protection using something called getters and setters. Think of getters as a way to "get" information, and setters as a way to "set" or change it. This way, you control how your gem is accessed and modified.

Here's a simple example to help you grasp the idea:

```java
public class GemCapsule {
    private String secretGem;

    public String getSecretGem() {
        return secretGem;
    }

    public void setSecretGem(String newGem) {
        secretGem = newGem;
    }
}

```

In this example, the secretGem is safely hidden inside the GemCapsule class. But you can still get its value using the getSecretGem method and change it using the setSecretGem method. This way, you're like the gatekeeper, controlling who accesses and modifies the gem.

This is a lot like how a capsule protects medicine. You can't just grab the medicine directly; you have to follow the instructions on the label. Encapsulation works similarly by providing controlled access to your code's important parts. It's like a security barrier that ensures your code stays solid and secure.

So, remember, encapsulation is your code's protective capsule. It guards your data, controls how it's used, and makes your code more organized. Happy coding!
