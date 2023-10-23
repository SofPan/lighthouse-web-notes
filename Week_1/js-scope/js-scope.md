# Scope in Javascript

A `Globally Scoped` variable is available everywhere in the code
  * If a variable is `globally scoped` and you call it before it is defined, it will be [hoisted](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting) and show as undefined.

A `Locally Scoped` variable is available in the function or code block where it is defined
  * If a variable is `locally scoped` and you call it outside it's code block, you will get a `reference error`.
  * If a local variable uses the same name as a global variable, the local variable takes precedence <i>inside its function</i>

It is ideal if functions avoid reading outer-scoped variables. If data is needed in the function, pass it in as a parameter