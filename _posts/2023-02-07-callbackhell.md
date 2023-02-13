---
title: TIL Call back hell and Promise chaining
date: 2023-02-07 09:00:00 +0100
categories: [JavaScript]
tags: [javascript, promises] # TAG names should always be lowercase
---

In asynchronous programming it happens that we need to nest callbacks within a function which is called a callback hell. In short, first we execute the first task, we get the result and task 2 needs to depend on result 1 to start its execution. Similarly, unless result 2 is produced we can't execute task 3. This leads to the chaining of tasks from 1 to 3, which creates a set of nested callbacks.
The problem is that this pyramid shaped set of codes is very difficult to follow and maintain. It kinda looks like this:

```javascript
getTodos("todos/luigi.json", (err, data) => {
  console.log(data);
  getTodos("todos/shaun.json", (err, data) => {
    console.log(data);
    getTodos("todos/mario.json", (err, data) => {
      console.log(data);
    });
  });
});
```

There are different solutions for avoiding callback hells such as using Promises or Async/await.
The idea of promise chaining is that the result is passed through the chain of .then handlers.
Our callback hell implemented by promises is going to look like this which is way more readable and cleaner:

```javascript
getTodos("todos/luigi.json")
  .then((data) => {
    console.log("promise resolved", data);
    return getTodos("todos/mario.json");
  })
  .then((data) => {
    console.log("promise2 resolved", data);
    return getTodos("todos/shaun.json");
  })
  .then((data) => {
    console.log("promise3 resolved", data);
  })
  .catch((err) => {
    console.log("promise rejected", err);
  });
```
