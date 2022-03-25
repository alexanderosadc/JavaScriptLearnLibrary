* Map
* Set
* WeakMap
* WeakSet

These data structures, introduced in ECMAScript Edition 6, take object references as keys. [`Set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set) and [`WeakSet`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakSet) represent a set of objects, while [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map) and [`WeakMap`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) associate a value to an object.

The difference between `Map`s and `WeakMap`s is that in the former, object keys can be enumerated over. This allows garbage collection optimizations in the latter case.

One could implement `Map`s and `Set`s in pure ECMAScript 5. However, since objects cannot be compared (in the sense of `<` "less than", for instance), look-up performance would necessarily be linear. Native implementations of them (including `WeakMap`s) can have look-up performance that is approximately logarithmic to constant time.