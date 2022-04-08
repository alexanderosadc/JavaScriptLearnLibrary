* `while`
* `do-while`
* `for (var i = 0; i < 5; i++)
* `for (let value of array)` - iterates over the values of iterable object;
* `for (let property in object)` - iterates over all enumerable property keys of an object; Iterating over a keys of a complex object;
* Another way of iterating over an array that was added with ECMAScript 5 is [`forEach()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach):
```
['dog', 'cat', 'hen'].forEach(function(currentValue, index, array) {
  // Do something with currentValue or array[index]
});
```

Arrays come with a number of methods. See also the [full documentation for array methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array).