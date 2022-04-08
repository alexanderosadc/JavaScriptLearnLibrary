[Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) are regular objects for which there is a particular relationship between integer-keyed properties and the `length` property.
[Typed Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Typed_arrays) are new to JavaScript with ECMAScript 2015, and present an array-like view of an underlying binary data buffer.

Arrays in JavaScript are actually a special type of object. They work very much like regular objects (numerical properties can naturally be accessed only using `[]` syntax) but they have one magic property called '`length`'. 
**This is always one more than the highest index in the array.**

```
var a = ['dog', 'cat', 'hen'];
a[100] = 'fox';
a.length; // 101
```

f you query a non-existent array index, you'll get a value of `undefined` in return:

```
typeof a[90]; // undefined
```

