JavaScript function declarations are allowed inside other functions.

An important detail of nested functions in JavaScript is that they can access variables in their parent function's scope:

```
function parentFunc() {
  var a = 1;

  function nestedFunc() {
    var b = 4; // parentFunc can't use this
    return a + b;
  }
  return nestedFunc(); // 5
}
```
