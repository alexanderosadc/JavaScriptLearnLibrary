`++`  = +1
`--`  = -1

## + Operator
The [`+` operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators#addition) also does string concatenation:
```
'hello' + ' world'; // "hello world"
```

If you add a string to a number (or other value) everything is converted into a string first. This might trip you up:

```
'3' + 4 + 5;  // "345"
 3 + 4 + '5'; // "75"
```

## && and || Operators
The `&&` and `||` operators use short-circuit logic, which means whether they will execute their second operand is dependent on the first. This is useful for checking for null objects before accessing their attributes:
```
var name = o && o.getName();
```

Or for caching values (when falsy values are invalid):

```
var name = cachedName || (cachedName = getName());
```

## Ternary Operator

```
var allowed = (age > 18) ? 'yes' : 'no';
```



