# Functions As Objects

In Javascript, functions are <i>first class objects</i>. This means:
  1. Functions can be stored in variables and passed around
  2. Functions can do everything other objects can do

Functions have properties and can even be assigned attributes.

## Callback Functions

  * A function passed (by reference) into another (receiver) function
  * Receiver is accepting behaviour to perform by calling the <u>callback</u> function it has access to
  * Receiver can call the callback at any time, as many times as it wants.

## Anonymous Functions

  * Unnamed functions that may or may not be assigned to a variable
  * Passed directly (inline) as an argument

## Arrow Functions

```Javascript
  // Arrow function syntax
  () => {}
  // can remove some characters for one-liners
  [1, 2, 3].forEach(num => console.log('num :', num));
  // Note single params do not need parentheses
  x => x * 2
```

<strong>Arrow functions do not get assigned a value for `this`</strong>