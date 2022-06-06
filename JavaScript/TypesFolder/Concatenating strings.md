# _template literal_ 
This can work just like a normal string, except you can include variables in it, wrapped inside `${ }` characters, and the variable's value will be inserted into the result:

const name = 'Chris';
const greeting = `Hello, ${name}`;
console.log(greeting); // "Hello, Chris"

const one = 'Hello, ';
const two = 'how are you?';
const joined = `${one}${two}`;
console.log(joined); // "Hello, how are you?"

# + Operator
```
const greeting = "Hello";
const name = "Chris";
console.log(greeting + ", " + name); // "Hello, Chris"
```

