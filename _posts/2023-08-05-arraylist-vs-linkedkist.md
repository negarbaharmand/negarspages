---
title: "TIL ArrayList vs. LinkedList in Java: Choosing the Right Tool for the Job"
date: 2023-08-05 09:52:00 +0200
categories: [JAVA, Collections]
tags: [java, collections] # TAG names should always be lowercase
---

Hey there, fellow Java enthusiasts!👩🏻‍💻
Today, I want to share a little discovery I made on my Java learning journey - the battle of ArrayList vs. LinkedList.

ArrayList and LinkedList are both classes that implement the List interface in Java. They allow you to store and manipulate collections of data, such as integers, strings, or custom objects. But here's where it gets interesting - they do it in different ways.

**ArrayList**: Think of an ArrayList as a dynamic array. It's like a resizable container that holds elements. When you add elements to an ArrayList, it keeps them in sequential memory positions. This makes ArrayLists excellent for quick access to elements using an index (like an array), but not so great when it comes to inserting or removing elements in the middle of the list.

**LinkedList**: In contrast, a LinkedList is a bit like a chain. Each element in a LinkedList is stored as a separate node, and each node points to the next one in line. This structure makes LinkedLists perfect for inserting or removing elements anywhere in the list but can be slower for direct access using an index.

Now,"When do I use which?"
If you need fast, random access to elements and your list doesn't change much after creation, go with an ArrayList. On the other hand, if you frequently insert or remove elements, especially in the middle of the list, a LinkedList might be your go-to choice.

Let's imagine this with a quick code example:

```java
import java.util.ArrayList;
import java.util.LinkedList;
import java.util.List;

public class ArrayListVsLinkedList {

   public static void main(String[] args) {
       List<String> arrayList = new ArrayList<>();
       List<String> linkedList = new LinkedList<>();

       // Adding elements
       arrayList.add("Negar's");
       linkedList.add("Negar's");

       // Adding an element in the middle
       arrayList.add(1, "coding!");
       linkedList.add(1, "coding!");

       // Accessing an element
       System.out.println("ArrayList: " + arrayList.get(1)); // Fast
       System.out.println("LinkedList: " + linkedList.get(1)); // Slightly slower

       // Removing an element
       arrayList.remove(1);
       linkedList.remove(1);
   }
}

```

In this example, we've created both ArrayList and LinkedList instances, added, accessed, and removed elements. As you can see, ArrayList provides faster access (thanks to indexing), while LinkedList shines when inserting or removing elements.

So, the next time you're working on a Java project and faced with the ArrayList vs. LinkedList dilemma, remember this post. Choose the data structure that suits your specific needs, and you'll be well on your way to writing more efficient and optimized code.
