```
// Note that there's no function name before the parentheses
let avg = function() {
  let sum = 0;
  for (const item of arguments) {
    sum += item;
  }
  return sum / arguments.length;
};
```

## Using function without by assigned
vaScript provides a mechanism for simultaneously declaring and invoking a function using a single expression. It's called an [Immediately invoked function expression (IIFE)](https://developer.mozilla.org/en-US/docs/Glossary/IIFE)

```
(function() {
  // …
})();
```