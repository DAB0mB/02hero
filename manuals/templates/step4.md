Conditional statements are used to perform different actions based on different conditions.

Very often when you write code, you want to perform different actions for different decisions. For this we can use conditional statements to to perform different actions based on different conditions.

```js
if (condition) {
  // block of code to be executed if the condition is true
}
```

![condition-flow](https://cloud.githubusercontent.com/assets/7648874/23193400/00eace7a-f890-11e6-8ec9-08c8a40946d4.png)

> Source: www.tutorialspoint.com

Before we go ahead and analyze the code snippet above, we need to understand exactly what a condition means in JavaScript. Conditions are code expressions which are being evaluated. If the resulting value is true, the given statement(s) are executed. If the expression is false, then the statement would not be executed. Most of the times, you will use **comparison operators** while making decisions.

## Comparison Operators

Comparison operators are used in logical statements to determine equality or difference between variables or values.

Given that `x = 5`, the table below explains the comparison operators:

| **Operator** | **Description**                   | **Comparing**             | **Returns**     | **Description** |
|--------------|-----------------------------------|---------------------------|-----------------|-----------------|
| ==           | equal to                          | x == 8 x == 5 x == "5"    | false true true | Addition        |
| ===          | equal value and equal type        | x === 5 x === "5"         | true false      | Subtraction     |
| !=           | not equal                         | x != 8                    | true            | Multiplication  |
| !==          | not equal value or not equal type | x !== 5 x !== "5" x !== 8 | false true true | Division        |
| >            | greater than                      | x > 8                     | false           | Modulus         |
| <            | less than                         | x < 8                     | true            | Increment       |
| >=           | greater than or equal to          | x >= 8                    | false           | Decrement       |
| <=           | less than or equal to             | x <= 8                    | true            |                 |

Comparison operators can be used in conditional statements to compare values and take action depending on the result.

```js
if (age < 18) text = "Too young";
```

Comparison operators can also be used along with **logical operators** when we want to represent a relationship between the two comparisons.

## Logical Operators

Logical operators are used to determine the logic between variables or values.

Given that `x = 6` and `y = 3`, the table below explains the logical operators:

| **Operator** | **Description** | **Comparing**      | **Returns** |
|--------------|-----------------|--------------------|-------------|
| &&           | and             | x < 10 && y > 1    | true        |
| \|\|         | or              | x == 5 \|\| y == 5 | false       |
| !            | not             | x == y             | true        |

Now that we went through all the necessary operators, lets try to have a better understanding of what a conditional statement is:

## Conditional Statements

In JavaScript we have the following conditional statements:

- Use `if` to specify a block of code to be executed, if a specified condition is true.
- Use `else` to specify a block of code to be executed, if the same condition is false.
- Use `else if` to specify a new condition to test, if the first condition is false.

### if

Use the `if` statement to specify a block of JavaScript code to be executed if a condition is true.

```js
if (condition) {
  // block of code to be executed if the condition is true
}
```

E.g. make a "Good day" greeting if the hour is less than 18:00:

```js
if (hour < 18) {
    greeting = "Good day";
}
```

Given that `hour = 17` the result of greeting will be "Good day".

### else

Use the `else` statement to specify a block of code to be executed if the condition is false.

```js
if (condition) {
  // block of code to be executed if the condition is true
} else {
  // block of code to be executed if the condition is false
}
```

E.g. if the hour is less than 18, create a "Good day" greeting, otherwise "Good evening":

```js
if (hour < 18) {
  greeting = "Good day";
} else {
  greeting = "Good evening";
}
```

Given that `hour = 19` the result of greeting will be "Good evening".

Note that specifically for assignments like shown in the code snippet above we can use the **Conditional (Ternary) Operator** which is a one-liner conditional assignment statement.

```js
greeting = hour < 18 ? "Good day" : "Good evening";
```

### else if

Use the `else if` statement to specify a new condition if the first condition is false.

```js
if (condition1) {
  // block of code to be executed if condition1 is true
} else if (condition2) {
  // block of code to be executed if the condition1 is false and condition2 is true
} else {
  // block of code to be executed if the condition1 is false and condition2 is false
}
```

E.g. if time is less than 10:00, create a "Good morning" greeting, if not, but time is less than 20:00, create a "Good day" greeting, otherwise a "Good evening":

```js
if (time < 10) {
    greeting = "Good morning";
} else if (time < 20) {
    greeting = "Good day";
} else {
    greeting = "Good evening";
}
```

Given that `time = 9` the result would be "Good morning".
