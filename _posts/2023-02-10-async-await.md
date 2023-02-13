---
title: TIL Writing more readable promises using async and await
date: 2023-02-10 09:00:00 +0100
categories: [JavaScript]
tags: [javascript, promises] # TAG names should always be lowercase
---

Using async and await, lets us section off all of our asynchronous code into a single asyncronous function and then use the await keyword inside, to chain promises together in a much more readable and logical way.
This is simply how Async and Await works:

- When we use async the function returns a promise.
- Inside the function we want to go and grab data so, we are going to use fetch api which returns a promise.
- Instead of using .then method, we use await
- This await keyword stops JavaScript from assigning a value to this variable until the promise has resolved. Once the promise has resolved we can take the value from that function (response) and assign it to this variable.
- As json method returns a promise we can again use the await keyyword to chain this promise.

- With using async and await we don’t use .then inside our asyncronous function where we are doing all of our promise chainings but we still need to do it once when we call an asyncronous function because it returns a promise and we don’t want it to be blocking.
- Here you can see the example code from the last post written using async and await:

```javascript
const getTodos = async (recourse) => {
  const res = await fetch(recourse);
  const data = await res.json();
  return data;
};
getTodos("todos/luigi.json").then((data) => {
  console.log("Success", data);
});
getTodos("todos/shaun.json").then((data) => {
  console.log("Success", data);
});
getTodos("todos/mario.json").then((data) => {
  console.log("Success", data);
});
```

Or

```javascript
const getTodos = async () => {
  const res = await fetch("todos/luigi.json");
  const data = await res.json();
  console.log(data);
  const res1 = await fetch("todos/shaun.json");
  const data1 = await res1.json();
  console.log(data1);
  const res2 = await fetch("todos/mario.json");
  const data2 = await res2.json();
  console.log(data);
};
getTodos();
```

- What have async and await acheived for us?

1. It has bundled up all of our asyncronous code inside a function which we can call and use whenever we want.
2. It’s an asyncronous function so it’s not going to block the rest of the code in our application.
3. It gives us a much cleaner way to chain promises together which is much more readable.
