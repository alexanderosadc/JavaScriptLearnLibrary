Strings in JavaScript are sequences of [Unicode characters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#unicode). This should be welcome news to anyone who has had to deal with internationalization. More accurately, they are sequences of UTF-16 code units; each code unit is represented by a 16-bit number. Each Unicode character is represented by either 1 or 2 code units.

*  It is a set of "elements" of 16-bit unsigned integer values;
* JavaScript strings are immutable;
* With conventions, it is possible to represent any data structure in a string;

# Functions
```
'hello'.length; // 5
```

```
'hello'.charAt(0); // "h"
'hello, world'.replace('world', 'mars'); // "hello, mars"
'hello'.toUpperCase(); // "HELLO"
```

# Multiline Strings
Template literals respect the line breaks in the source code, so you can write strings that span multiple lines like this:

```
const output = `I like the song.
I gave it a score of 90%.`;
console.log(output);  // I like the song.
                      // I gave it a score of 90%.
```

# Retrieving a specific string character
```
browserType[0];
```

```
browserType[browserType.length-1];
```

# Testing if a string contains a substring
```
browserType.includes('zilla')
```

```
browserType.startsWith('zilla')
```

```
browserType.endsWith('zilla')
```

```
tagline.indexOf('developers')
```

```
const browserType = 'mozilla';
console.log(browserType.slice(1, 4)); // "ozi"
```

```
const browserType = 'mozilla';
const updated = browserType.replace('moz','van');

console.log(updated);      // "vanilla"
console.log(browserType);  // "mozilla"
```



[[Concatenating strings]]
