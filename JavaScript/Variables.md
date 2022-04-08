`let` - block level variables;

```
// myLetVariable is *not* visible out here

for (let myLetVariable = 0; myLetVariable < 5; myLetVariable++) {
  // myLetVariable is only visible in here
}

// myLetVariable is *not* visible out here
```

`const` - constant. Avialiable from the block it was declared;

```
const Pi = 3.14; // variable Pi is set
Pi = 1; // will throw an error because you cannot change a constant variable.
```

`var` - variable avialiable from the function it is declared. Global variable;

An example of scope with a variable declared with **`var`:**

```
// myVarVariable *is* visible out here

for (var myVarVariable = 0; myVarVariable < 5; myVarVariable++) {
  // myVarVariable is visible to the whole function
}

// myVarVariable *is* visible out here
```

If you declare a variable without assigning any value to it, its type is `undefined`.

## An important difference between JavaScript and other languages like Java is that in JavaScript, blocks do not have scope; only functions have a scope.
