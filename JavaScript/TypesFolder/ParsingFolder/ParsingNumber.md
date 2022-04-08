# Parse Int
```
parseInt('123', 10); // 123
parseInt('010', 10); // 10
```

In older browsers, strings beginning with a "0" are assumed to be in octal (radix 8), but this hasn't been the case since 2013 or so. Unless you're certain of your string format, you can get surprising results on those older browsers:

```
parseInt('010');  //  8
parseInt('0x10'); // 16
```

If you want to convert a binary number to an integer, just change the base:

```
parseInt('11', 2); // 3
```

# Parse Float
`parseFloat()` always uses base 10.

# + Operator

You can also use the unary `+` operator to convert values to numbers:

```
+ '42';   // 42
+ '010';  // 10
+ '0x10'; // 16
```

A special value called [`NaN`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/NaN) (short for "Not a Number") is returned if the string is non-numeric:

```
parseInt('hello', 10); // NaN
```
