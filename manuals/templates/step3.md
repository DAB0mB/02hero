JavaScript operators are used to assign values, compare values, perform arithmetic operations, and more. In this step, we will learn about arithmetic operators in specific, since they are the most basic, but we will go through all available operators in the language as we go further in this tutorial.

Arithmetic operators perform arithmetic on numbers (literals or variables).

| **Operator** | **Description** |
|--------------|-----------------|
| +            | Addition        |
| -            | Subtraction     |
| *            | Multiplication  |
| /            | Division        |
| %            | Modulus         |
| ++           | Increment       |
| --           | Decrement       |

A typical arithmetic operation operates on two numbers. The two numbers can be literals

```js
var x = 100 + 50;
```

or variables

```js
var x = a + b;
```

or expressions.

```js
var x = (100 + 50) * a;
```

Note that the parenthesis play a very important role. Just in math, expressions in parenthesis will be calculated first by their nesting order.

```js
var x = ((100 + 50) + 2) * 2; // 304
var y = (100 + 50) + (2 * 2); // 154
```

The numbers (in an arithmetic operation) are called operands. The operation (to be performed between the two operands) is defined by an operator.

```js
var x = 1  // operand
        +  // operator
        2; // operand
```

Now let's dive in to each of the operators and see how we can use them.

### addition

The addition operator (`+`) adds numbers.

```js
var x = 5;
var y = 2;
var z = x + y;
```

### subtraction

The subtraction operator (`-`) subtracts numbers.

```js
var x = 5;
var y = 2;
var z = x - y;
```

### multiplication

The multiplication operator (`*`) multiplies numbers.

```js
var x = 5;
var y = 2;
var z = x * y;
```

### division

The division operator (`/`) divides numbers.

```js
var x = 5;
var y = 2;
var z = x / y;
```

The modular operator (`%`) returns the division remainder.

### modulus

```js
var x = 5;
var y = 2;
var z = x % y;
```

### increment

The increment operator (`++`) increments numbers.

```js
var x = 5;
x++;
var z = x;
```

The increment operator doesn't necessarily have to used as a postfix, it can also be used as a suffix.

```js
var x = 5;
++x;
var z = x;
```

Be careful when changing the position of the operator, the difference is crucial. When using the operator as a postfix, the operand will be returned and **only then** it will be incremented. On the other hand, when the operator is used as a prefix, the operand will be incremented before it is returned.

```js
var a = 0;
var b = ++a; // b is 1, a is 1
var c = a++; // c is 1, a is 2
```

### decrement

The decrement operator (`--`) decrements numbers.

```js
var x = 5;
x--;
var z = x;
```

The decrement operator doesn't necessarily have to used as a postfix, it can also be used as a suffix.

```js
var x = 5;
--x;
var z = x;
```

Just like the increment operator, the position of the operator matters.

```js
var a = 1;
var b = --a; // b is 0, a is 0
var c = a--; // c is 0, a is -1
```

## Operator Precedence

Operator precedence describes the order in which operations are performed in an arithmetic expression.

```js
var x = 100 + 50 * 3;
```

Is the result of example above the same as 150 * 3, or is it the same as 100 + 150? Is the addition or the multiplication done first? As in traditional school mathematics, the multiplication is done first. Multiplication (`*`) and division (`/`) have higher precedence than addition (`+`) and subtraction (`-`). And (as in school mathematics) the precedence can be changed by using parentheses.

```js
var x = (100 + 50) * 3;
```

When using parentheses, the operations inside the parentheses are computed first. When many operations have the same precedence (like addition and subtraction), they are computed from left to right.

```js
var x = 100 + 50 - 3;
```

## Infinity

The `Infinity` value represents a number whose value is not finite. You will most likely encounter a result with such value when trying to divide by `0`.

```js
var num = 100 / 0; // Infinity
```

`Infinity` can be a negative value as well.

```js
var num = -100 / 0; // -Infinity
```

## NaN

The `NaN` value stands for "Not-a-Number". This value indicates that a value is not a legal number, and can be resulted once an illegal arithmetic operation was performed.

```js
var x = 0 / 0; // NaN
var y = 1 / undefined; // NaN
```

---

These were arithmetic operations on a nutshell. There are lots of edge cases we haven't talked about, but we will go through them further in this tutorial. In the next step we will learn about conditional statements and how we can use them to perform different actions based on conditions.