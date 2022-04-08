```
class Professor extends Person {

  teaches;

  constructor(name, teaches) {
    super(name);
    this.teaches = teaches;
  }

  introduceSelf() {
    console.log(`My name is ${this.name}, and I will be your ${this.teaches} professor.`);
  }

  grade(paper) {
    const grade = Math.floor(Math.random() * (5 - 1) + 1);
    console.log(grade);
  }

}
```

Since we want to set `teaches` when a new `Professor` is created, we define a constructor, which takes the `name` and `teaches` as arguments. The first thing this constructor does is call the superclass constructor using [`super()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/super), passing up the `name` parameter. The superclass constructor takes care of setting `name`. After that the `Professor` constructor sets the `teaches` property.

**Note:** If a subclass has any of its own initialization to do, it **must** first call the superclass constructor using `super()`, passing up any parameters that the superclass constructor is expecting.
