---
title: What I learnt today:"this" keyword in JavaScript
date: 2023-01-23 09:00:00 +0100
categories: [JavaScript]
tags: [javascript, wilt] # TAG names should always be lowercase
---

In JavaScript, the "this" keyword is used to refer to the current object. It can be used within an object's method to refer to the object itself, or it can be used alone to refer to the global window object.
It is also used to refer to the object that a function is a method of. It provides a way to access the object from within the function.
In the code below "this" refers to the object "user":

```JavaScript
let user = {
  name: "Negar",
  age: 32,
  email: "ngdezfouli@gmail.com",
  log: function () {
    console.log(this);
  },
};
user.log();
```

And the result is showed on console like:

```
{name: 'Negar', age: 32, email: 'ngdezfouli@gmail.com', log: ƒ}
age: 32
email: "ngdezfouli@gmail.com"
log: ƒ ()
name: "Negar"
[[Prototype]]: Object
```

But if we use "this" out of the scope :

```JavaScript
let user = {
  name: "Negar",
  age: 32,
  email: "ngdezfouli@gmail.com",
};
console.log(this);

```

The result would be shown as this:

```
Window {window: Window, self: Window, document: document, name: '', location: Location, …}
```

We should also be aware that If we use "this" inside an arrow function it's going to address the global window object, not our object! So, to use "this" inside a method to refer to the actual object that the method is on, we need to use a regular function and not an arrow function.
