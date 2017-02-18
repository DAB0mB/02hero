JavaScript consists of 5 primitives: [number](#number), [boolean](#boolean), [string](#string), [undefined](#undefined) and [null](#null). Let's have a brief introduction for each of them:

### number

JavaScript numbers are always 64-bit floating point. There's no such thing as `int`, `double`, `float`, `unsigned int` or `long double`, just type the number the way you want and you're good to go.

```js
var intNumber = 123;
var floatNumber = 123.45;
```

### boolean

Very often, in programming, you will need a data type that can only have one of two values, like

- yes / no.
- on / off.
- true / false.

For this, JavaScript has a `boolean` data type. It can only take the values `true` or `false`.

```js
var truthyBool = true;
var falsyBool = false;
```

You can use the `Boolean()` function which is pre-defined in the environment to convert other data-types to booleans.

```js
var truthyBool = Boolean(1); // true
var falsyBool = Boolean(0);  // false
```

Everything that has "real" value will be converted to `true` and everything that has an "empty" value will be converted to `false`.

Examples of truthy values:
- `1` (anything but `0`)
- `"string"` (anything but an empty string)

Examples of falsy values:
- `0`
- `""` (empty string)
- `null`
- `undefined`

> Note that negative numbers are **not** falsy, neither do strings whose value is `"0"` (because `"0"` is being mapped to `48` according to the ASCII table).

### string

A JavaScript string simply stores a series of characters like "John Doe". A string can be any text inside quotes. You can use single or double quotes.

```js
var carname = "Volvo XC60";
var carname = 'Volvo XC60';
```

You can use quotes inside a string, as long as they don't match the quotes surrounding the string.

```js
var answer = "It's alright";
var answer = "He is called 'Johnny'";
var answer = 'He is called "Johnny"';
```

Because strings must be written within quotes, JavaScript will misunderstand this string.

```js
var y = "We are the so-called "Vikings" from the north."
```

The string will be chopped to "We are the so-called ". The solution to avoid this problem, is to use the `\` escape character. The backslash escape character turns special characters into string characters.

```js
var x = 'It\'s alright';
var y = "We are the so-called \"Vikings\" from the north."
```

The escape character (`\`) can also be used to insert other special characters in a string.

These are commonly used special characters that can be inserted in a text with the backslash sign:

| **Code** | **Outputs**  |
|----------|--------------|
| \'       | single quote |
| \"       | double quote |
| \\       | backslash    |

Five other escape characters are valid in JavaScript:

| **Code** | **Outputs**          |
|----------|----------------------|
| \b       | Backspace            |
| \r       | Carriage Return      |
| \f       | Form Feed            |
| \t       | Horizontal Tabulator |
| \v       | Vertical Tabulator   |

### undefined

The `undefined` value indicates that a variable has not been assigned a value, and is written with a literal, `undefined`.

```js
var x; // undefined
```

Although not very common, you can manually set a variable to be `undefined` (`null` is preferred, a matter of convention).

```js
var x = 123;
x = undefined;
```

### null

The value `null` is written with a literal, `null`. In most JavaScript projects `null` is often retrieved in place where an object can be expected but no object is relevant.

```js
var num = 123;
num = null; // number is expected, but non exists
```

---

This was a nice introduction for primitives, but keep in mind that there are things that we haven't gone through yet. We first need to learn things which are crucial for us to understand, and only then we can get back to this topic in more detail. Up next, we will learn about arithmetic operators, and how we can use them in JavaScript to make different calculations.
