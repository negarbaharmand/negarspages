---
title:TIL Async and Await
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
