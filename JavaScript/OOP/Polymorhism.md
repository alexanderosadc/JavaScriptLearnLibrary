### Function Overloading

``` 
// Volume of a Cube. 
int Volume(int s) 
{ return s * s * s; } 

// Volume of a Cuboid. 
long Volume(long l, int b, int h) 
{ return l * b * h; }
```


![[Pasted image 20220328002816.png]]

### Coercion Polymorphism
JavaScript has Type coercion. It converts value from one type to another while evaluating them.
For example, you can any expression inside an `if` statement. JavaScript converts expression into `true` or `false`. If the expression converts to `true`, the expression is said to be truthy. If the expression converts to `false`, the expression is said to be falsey.

![[Pasted image 20220328002905.png]]


Another example: You can compare strings and numbers with `==` (although this is generally not recommended).
`22 == '22'`
