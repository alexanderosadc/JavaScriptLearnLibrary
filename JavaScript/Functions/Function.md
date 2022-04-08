Every JavaScript function is actually a `Function` object. This can be seen with the code `(function(){}).constructor === Function`, which returns true.

```
function add(x, y) {
  const total = x + y;
  return total;
}
```


The `return` statement can be used to return a value at any time, terminating the function. If no return statement is used (or an empty return with no value), JavaScript returns `undefined`.

t to be more like guidelines than anything else. You can call a function without passing the parameters it expects, in which case they will be set to `undefined`.

```
add(); // NaN
// You can't perform addition on undefined
```

Copy to Clipboard

You can also pass in more arguments than the function is expecting:

```
add(2, 3, 4); // 5
// added the first two; 4 was ignored
```


That may seem a little silly, but functions have access to an additional variable inside their body called [`arguments`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments), which is an array-like object holding all of the values passed to the function. Let's re-write the add function to take as many values as we want:

```
function add() {
  let sum = 0;
  for (const item of arguments) {
    sum += item;
  }
  return sum;
}

add(2, 3, 4, 5); // 14
```

## Rest Parameter Syntax

 [Rest parameter syntax](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters). In this way, we can pass in any number of arguments into the function while keeping our code minimal. The **rest parameter operator** is used in function parameter lists with the format: **...variable** and it will include within that variable the entire list of uncaptured arguments that the function was called with.

```
function avg(...args) {
  let sum = 0;
  for (const item of args) {
    sum += item;
  }
  return sum / args.length;
}

avg(2, 3, 4, 5); // 3.5
```


## Apply function
 The `avg()` function takes a comma-separated list of arguments — but what if you want to find the average of an array? You could just rewrite the function as follows:
```
function avgArray(arr) {
  let sum = 0;
  for (const item of arr) {
    sum += item;
  }
  return sum / arr.length;
}

avgArray([2, 3, 4, 5]); // 3.5
```

Copy to Clipboard

But it would be nice to be able to reuse the function that we've already created. Luckily, JavaScript lets you call a function with an arbitrary array of arguments, using the [`apply()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/apply) method of any function object.

```
avg.apply(null, [2, 3, 4, 5]); // 3.5
```

## Spread Syntax

Allows an iterable such as an array expression or string to be expanded in places where zero or more arguments (for function calls) or elements (for array literals) are expected, or an object expression to be expanded in places where zero or more key-value pairs (for object literals) are expected.

```
function sum(x, y, z) {
  return x + y + z;
}

const numbers = [1, 2, 3];

console.log(sum(...numbers));
// expected output: 6

console.log(sum.apply(null, numbers));
// expected output: 6
```

- [[AnonymousFunctions]]
- [[RecursiveFunctions]]
- [[InnerFunctions]]
- [[Closures]]
- [[FunctionObjectConstructor]]