# Objects

## Primitive Data Types
In Javascript, all values which are not Objects are referred to as primitives.
  * Undefined
  * Null
  * Boolean
  * String
  * Number
  * Symbol (introduced in ES6)

Anything not on the above list is an object. All objects have properties.

## Objects - Basic Concepts
Objects:
  1. Keys are always strings
  2. Each key is unique (once per object)
  3. Each key has exactly one value

Object syntax uses braces `{}`.
  ```Javascript
    const object = {};
    const tinyObj = {size: "tiny"};
  ```

Keys do not need quotes, except when:
  * The key has spaces or hyphens in it
  * When you need to access the key outside the object and you are using square brackets

You access the key's value by calling it with the object using square brackets or a period:
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