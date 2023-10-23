# Function Best Practices

### A pure function is:
  * specific
  * value producing
  * has no side-effects
  * does not rely on side-effects from other code

### Function Rules
  * Name functions properly. A good name is short and describes what a function does as unambiguously as possible
  * Begin function names with action words like `createUser` or `sendUserData`
  * `camelCase` function names
  * Proper indentation is key
    ```Javascript
      const createFunction = () => {
        let tabbedVariable = true;
      let badlyTabbedVariable = "yuck";
      }
    ```
  * Data needed by functions should be passed in as a parameter