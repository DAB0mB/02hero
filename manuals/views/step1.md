[{]: <region> (header)
# Step 1: Variables
[}]: #
[{]: <region> (body)
Unlike a traditional high-level programming language (e.g. Java, C++) which is being compiled ahead of time into an executable, JavaScript, as the name suggests, is a [scripting language](https://en.wikipedia.org/wiki/Scripting_language), which means that it is being interpreted during run-time by an [interpreter](https://en.wikipedia.org/wiki/Interpreter_(computing)) (rather than being compiled by a compiler). The fact that a script doesn't have to be compiled gives it the advantage of being able to use dynamic variables, meaning we don't have to declare specific data-types like `int` or `double`, instead we can just use the `var` keyword generally.

```js
var numberVariable = 1;
var booleanVariable = true;
```

> Most JavaScript programs' naming convention is based on the [camelCase](https://en.wikipedia.org/wiki/Camel_case) practice; It means that variables will be named using words or phrases such that each word or abbreviation in the middle of the phrase begins with a capital letter, with no intervening spaces or punctuation. Common examples include "iPhone", "eBay", "FedEx", and "HarperCollins". Eventually each program has its own set of conventions, so I'm not going to dwell on writing style, except for things which are a must and you will find them in 99% of the projects.

Further more, we can dynamically change the data-type of a variable, even though it was declared else wise.

```js
var numberVariable = 1;
var booleanVariable = true;
numberVariable = true;
booleanVariable = 1;
```

Indeed, it greatly accelerates the development process, but it comes with a drawback. The fact that data-types can be suddenly changed means that the interpreter needs to check the data-type of the inserted value each interpretation (is it n `double`? Or is it a `boolean`?), something which takes precious time and being reflected in performance. For that very reason, it's hard to believe that JavaScript is ever going to be a worthy competitor against compiled languages when it comes to performance. If you were being taught in university that performance is everything then, I will have to disappoint, but the web developers have chosen JavaScript over traditional programming languages and for a good reason.

In many cases you will find yourself wanting to store complex duplicate values in a variable to prevent them from being hard coded. For that purpose, JavaScript allows you to define constant variables using the `const` keyword, which will prevent them from being reset.

```js
const GOLDEN_RATIO = 1.6180339887;
GOLDEN_RATIO = 0; // Throws an error
```

> Some programs will name constant variables based on the [snake_case](https://en.wikipedia.org/wiki/snake_case) practice.

As you can probably figure out from the code snippet above, you can write comments using the `//` prefix.

```js
// number variable
var numberVariable = 1;
// boolean variable
var booleanVariable = true;
```

Alternatively, you can define comment blocks using `/*` as a prefix and `*/` as a postfix.

```js
/*
  Variables definition
 */

var numberVariable = 1;
var booleanVariable = true;
```

When skipping a line you don't necessarily have to use a semicolon (`;`)

```js
var numberVariable = 1
var booleanVariable = true
```

but you have to do so whenever you want to write multiple commands in a single line.

```js
var numberVariable = 1; var booleanVariable = true;
```

Most JavaScript projects across the net do use a semicolon at the end of a line, because it's a clear and easy way to say: "Hey, I finished". You can also write a single command using multiple lines.

```js
var sum = 1 + 2 +
          3 + 4;
```

JavaScript ignores multiple spaces. You can add white space to your script to make it more readable.

The following lines are equivalent:

```js
var person = "Hege";
var person="Hege";
```

A good practice is to put spaces around operators (`=`, `+`, `-`, `*` and `/`).

```js
var x = y + z;
```

So that's it for the current step. We've learned about the very basics of dynamic variables deceleration in JavaScript, and how we can use it. Obviously we have a lot more to go through, but now people who've never seen JavaScript before in their lives can start building their basis. In the next step we will go through all available primitive values in JavaScript, discuss about them, and see how they can interact with each other.

[}]: #
[{]: <region> (footer)
[{]: <helper> (nav_step)
| [< Intro](../../README.md) | [Next Step >](step2.md) |
|:--------------------------------|--------------------------------:|
[}]: #
[}]: #