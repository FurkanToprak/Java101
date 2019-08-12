---
tags: [Java101]
title: 'lesson6'
created: '2019-08-12T15:31:55.849Z'
modified: '2019-08-12T18:26:53.747Z'
---

# Java 101 | Lesson 6:
## Booleans:
Let's review what booleans are. A `boolean` is a data type that can indicate whether something is `true` or `false`. `true` and `false` are similar to `yes` and `no`, or `on` and `off`.
## Boolean Expressions:
Boolean expressions are statements in programming that can evaluate to `true` or `false`. 

You can think of boolean expressions as questions. The expression `4 < 5` can be rephrased as "Is 4 less than 5?". The answer to this question, how the expression is _evaluated_, is `true`.

You can also store booleans like below:
```Java
boolean mathCondition = 4 < 5;
```

Here are some similar logical operators:
* `<` is the less than operator.
  * `A < B` can be rephrased the question "is A less than B?"
* `>` is the greater than operator.
  * `A > B` can be rephrased the question "is A greater than B?"
* `==` is the equal to operator.
  * `A == B` can be rephrased the question "is A equal to B?"

Here are some examples demonstrating logical operator:
```Java
boolean example1 = 4 < 5;
boolean example2 = 4 > 5;
boolean example3 = 4 == 5;
```
## Basic Boolean Operators and Truth Tables:
Say we wanted to express more complicated questions as boolean expressions. For example, if we wanted to ask the question "is what I'm holding a red apple?", we would have to break it down into two questions:
1) Is what I'm holding red?
2) Is what I'm holding an apple?
For something to be considered a red apple, it has to be red **and** an apple.
Similarly, we can combine two boolean expression to make one more complex boolean expression.
### And (`&&`):
`true && true`: `true`
`true && false`: `false`
`false && true`: `false`
`false && false`: `false`
Let's demonstrate this with examples:
```Java
boolean isRedApple = isRed && isApple;
```
* When `isRed` is `true` and `isApple` is `true`, `isRedApple` is `true`.
* When `isRed` is `true` and `isApple` is `false`, `isRedApple` is `false`.
* When `isRed` is `true` and `isApple` is `true`, `isRedApple` is `false`.
* When `isRed` is `true` and `isApple` is `true`, `isRedApple` is `false`.
### Or (`||`):
`true || true`: `true`
`true || false`: `true`
`false || true`: `true`
`false || false`: `false`
Let's demonstrate this with examples:
```Java
boolean isVehicle = isCar || isTruck;
```
* When `isCar` is `true` and `isTruck` is `true`, `isVehicle` is `true`.
* When `isCar` is `true` and `isTruck` is `false`, `isVehicle` is `true`.
* When `isCar` is `true` and `isTruck` is `true`, `isVehicle` is `true`.
* When `isCar` is `true` and `isTruck` is `true`, `isVehicle` is `false`.
### Not (`!`):
`!true`: `false`
`!false`: `true`
This operator turns a boolean into the opposite boolean. Let's demonstrate this with examples:
```Java
boolean isHot = !isCold;
```
* When `isHot` is `true`, `isCold` is `false`.
* When `isHot` is `false`, `isCold` is `true`.
## Conditions (if, else if, else):
The founding fathers of computers, Alan Turing and Charles Babbage, realized early on for a computer to be a machine that can _truly_ be useful, it must be able to have **conditional branching**. Conditional branching is the act of only executing code _if_ a certain statement is true. For conditional branching, we use **if statements** in programming. Let's show an example of conditional branching:
```Java
boolean mathCondition = 4 < 5;
if (mathCondition) {
  System.out.println("4 is less than 5.");
}
```
Here is the output:
`4 is less than 5.`
The code block following the if statement executed because condition following the if statement evaluated to `true`. Here's a more generic example:
```Java
if (true)
{
  System.out.println("This code will execute.");
}

if (false)
{
  System.out.println("This code will not execute.");
}
```
The output is `This code will execute.` The statement within the if statement that evaluated to false did not execute. We can make more advanced conditions as well by adding `else if` and `else` statements. Let's look at an intuitive example as to how if, if else, and else statements work before reviewing the way they function.
```Java
// an int variable called someNumber was declared and assigned a value earlier in the code.
if (someNumber < 0) {
    System.out.println("The number is negative.");
}
else if (someNumber == 0) {
    System.out.println("The number is zero.");
}
else {
    System.out.println("The number is positive.");
}
```
Here's how if, if else, and else statements work:
* The if statement is checked. If it evaulates to `true`, the code within the if statement is executed and the code within the `else if` and `else` statements are skipped (not executed).
* Under the condition that the if statement is `false`, the condition within the else if statement is checked. You can have multiple else if statements. The first else if statement to be evalutated as true executes.
* If none of the if or else if statements evaluate as true, the else statement is executed.
Let's use another example to show how multiple else if statements work:
```Java
// an int variable called someNumber was declared and assigned a value earlier in the code.
if (someNumber < -100) {
    System.out.println("The number is a very small negative number.");
}
else if (someNumber < 0) {
    System.out.println("This number is negative.");
}
else if (someNumber == 0) {
    System.out.println("The number is zero.");
}
else if (someNumber > 100) {
    System.out.println("This number is a very large positive number.");
}
else {
    System.out.println("The number is positive.");
}
```
* If someNumber is -121, the output is `The number is a very small negative number.`
* If somenumber is -81, the output is `This number is negative.`
* If someNumber is 0, the output is `The number is zero.`
* If someNumber is 309, the output is `This number is a very large positive number.`
* If someNumber is 22, the output is `The number is positive.`
## Loops:

### While Loops:

### For Loops:
