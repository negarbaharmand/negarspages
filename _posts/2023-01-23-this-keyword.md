---
title: What I learnt today (WILT): "this" keyword in JavaScript
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
