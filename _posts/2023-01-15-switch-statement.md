---
title: How to use switch statement in JavaScript and emulate it in Python?
date: 2023-02-15 09:00:00 +0100
categories: [Conditionals, Python, JavaScript]
tags: [js, python] # TAG names should always be lowercase
---

In JavaScript, a switch statement is used to perform different actions based on different conditions. It is a control flow statement that tests a given expression against a set of cases, and executes the block of code associated with the matching case. The switch statement is typically used as an alternative to a series of if-else statements, when you have multiple conditions that need to be tested against a single expression.

```javascript
switch (x) {
  case 0:
    // do something
    break;
  case 1:
    // do something else
    break;
  default:
    // do a third thing
    break;
}
```

To emulate this functionality in Python, we could use a series of if-elif-else statements:

```python
if x == 0:
    # do something
elif x == 1:
    # do something else
else:
    # do a third thing
```

Alternatively, we can use a dictionary to map values to actions, in the following way:

```python
def zero():
    print("zero")

def one():
    print("one")

def default():
    print("default")

options = {0: zero, 1: one}

options.get(x, default)()
```
