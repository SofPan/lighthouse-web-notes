# Objects

## Primitive Data Types
In Javascript, all values which are not Objects are referred to as primitives.
  * Undefined
  * Null
  * Boolean
  * String
  * Number
  * Symbol (introduced in ES6)
  * BigInt

Anything not on the above list is an object. All objects have properties.

Primitives are immutable. They can be redefined but the original value is not changed in memory.

Primitives are passed to a function by value, this means the function gets a copy of the primitive.

## Objects - Basic Concepts
Objects:
  1. Keys are always strings
  2. Each key is unique (once per object)
    a) Nested objects can use a key name present in the parent object
  3. Each key has exactly one value
  4. Objects are mutable (contents can be changed)
  5. Objects are passed to functions by reference, this means the original is obtained and gets changed directly

Object syntax uses braces `{}`.
  ```Javascript
    const object = {};
    const tinyObj = {size: "tiny"};
  ```

Keys do not need quotes, except when:
  * The key has spaces or hyphens in it
  * When you need to access the key outside the object and you are using square brackets

You access the key's value by calling it with the object using square brackets or dot-syntax:
  ```Javascript
    tinyObj["size"] // "tiny"
    tinyObj.size // also "tiny"
  ```

Square brackets can also be used to assign new values to existing keys, or create new key-value pairs:
  ```Javascript
  const mary = {name: "Mary Sue"};
  mary["name"] = "Mary Jane";
  mary["age"] = 22;
  mary; //shows resulting object {name: "Mary Jane", age: 22}
  ```

 #### A note on dot-syntax
 If the key is a variable, dot-syntax will not work. There are some other instances as well where square brackets are a must.

### Nested Objects as values

```Javascript
  const person = {
    name: "Paul",
    address: {
      street: "310 W 95th",
      city: "New York",
      zipCode: 10027
    }
  }
```

Use square brackets to access nested values:
```Javascript
  person["address"]["city"] // "New York"
```
Object.keys(...) returns an array of keys

## Objects - Iteration

Use a for...in loop to iterate over an object's keys

```Javascript
  for (let key in object) {
    ley keyValue = object[key];
    console.log("The value of" + key + "is" + keyValue);
  }
```