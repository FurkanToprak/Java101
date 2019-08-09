---
tags: [Java101]
title: lesson5
created: '2019-08-07T13:23:06.953Z'
modified: '2019-08-09T17:44:22.957Z'
---

# Lesson 5 | Libraries and Math in Java:
## Libraries:
Let's picture that we have become Java programmers and that we specifically love making games in Java that include cars. It would be quite a repetitive task to have to code a car class every time. Instead, we should just code a `Car` class once and _reuse_ the code. This is where libraries come in.

Libraries allow for **reusability** of code. Libraries are collections of code that provide classes with useful attributes for the programmer. We store our useful libraries within **packages**. Packages are collections of codes. For our example, let's call our package `useful_package`. Let's say that the `Car` class exists within a `Car.java` file within the package. If we wanted to use that code, we would have to **import** it. Here's how to import an item from a package:
```Java
// The format is import <package>.<class>
import useful_package.Car;
```
## Math in Java:
Before we proceed with this course, let us think about why we _need_ computers. Computers are very good at _computing_. This is why the first applications for computers were used for mathematics. Similarly, to be able to use computers to their fullest capabilities, we must learn how math works in programming and in Java specifically. Let's get started.
### Review:
* Before we start, we'll have to review [our data types from earlier.](https://github.com/FurkanToprak/Java101/blob/master/lesson3.md#data-types)
* We use `f` and `d` at the end of floats and decimals to let Java distinguish decimals between `float` and `double`s. This is important because Java won't be able to store doubles within a float. For example, ```float a = 2.3``` will not compile. The reason for this is because Java sees explicitly written decimals as doubles by default. By this, we mean that Java sees the number `2.3` and assumes that it is a `double`. For this reason, we must indicate that `2.3` is a float by using the letter `f`, like so: `float a = 2.3f`. Although `double` doesn't require this because it is the largest possible data type for storing numbers, it's good practice to still include the `d` at the end of `double`s for now. As you become more experienced, you may stop using `d` if you feel that it clutters code, but it's a good reminder for beginners.
 * Let's review this: `float` variables _must_ end with `f`. `double` variables _don't have to_ end with `d`, but it's a good idea to add it in for now. Here's what it should look like:
 ```Java
 float a = 3.1415f;
 double b = 3.1415d;
 ```
 **Note:** The addition section is much longer than subtraction, multiplication and division. This is because we'll be using addition examples to learn new concepts.

### Addition:
The addition operator in Java is `+`. Now that we know that, let's make use of this:
```Java
int a = 5;
int b = 3;
int c = 5 + 3;
System.out.println(c); // 8
float d = 4.3f;
float e = 3.2f;
float f = d + e;
System.out.println(f); // 7.5
double g = 4.3;
double h = 3.2;
double i = g + h;
System.out.println(i); // 7.5
```
If you've noticed, we've only added variables from the same data types. When adding data types, it gets a bit trickier. Here are the rules:
* Make sure if you combine two data variables, the variable in which you store the result is of the same data type as the largest data type in the additive expression. Here's an example of this:
```Java
float a = 99.99f; // The float data type is 4 bytes.
double b = 0.01d; // The double data type is 8 bytes. Double can also store more decimals and larger numbers.
/*
  Now, we'll need to store a + b in a variable called c. When combining two numberical data types, the resulting value must be of the same data type as the largest data type used in the mathematical expression. This is why c must be a double.
*/
double c = a + b;
```
Here is a quick example with `byte`, `short`, `int` and `long`.
```Java
long a = 12;
int b = 3;
short c = 345;
byte d = 125;
/*
  If we want to make a variable, e, that is a + b + c, we'll need to make e the largest data type from the three variables. long is 8 bytes, int is 4 bytes, short is 2 bytes, and a byte is 1 byte. Therefore, e must be long.
*/
long e = a + b + c + d;
```

```Java
double a = 99.99d;
double b = 0.01d;
/*
  You also can't store whole numbers that are stored in floats or doubles within byte, short, int, or long.
  Even though a + b is (in normal mathematics) 100, in Java a + b = 100.00 (as a double). For this reason
  we can't store a + b within a whole number data type such as byte, short, int, or long.
*/
double c = a + b;
System.out.println(c); // 100.00
```
**Numerical Conversion:**
* If you do try to store a large data type in a small data type, you'll get the following error: `error: incompatible types: possible lossy conversion from <large data type> to <small data type>`. For example, if we tried to make `e` an `int`, we'd get the following error: `error: incompatible types: possible lossy conversion from long to int`.
* We can, however, store a smaller data variable within a larger one. Here are some examples:
```Java
// Let's store a float within a double.
double a = 12.4f;
// Let's store an int within a long.
int b = 4;
long c = b;
```
### Subtraction:
The subtraction operator in Java is `-`. The same rules apply regarding data types. Here are some quick examples:
```Java
double a = 2356.3d;
double b = 321.2d;
double c = a - b;

double e = 12.043d;
float f = 23.3f;
double g = e - f;

double h = 1.3;
double i = 0.3;
double j = h - i; // Double, not int- even if the answer is 1 in "normal" mathematics!
```
### Multiplication:
The subtraction operator in Java is `*`. Again, the same rules apply regarding data types. Here are some quick examples:
```Java
double a = 2356.3d;
double b = 321.2d;
double c = a * b;

double e = 12.043d;
float f = 23.3f;
double g = e * f;

double h = 10.0d;
double i = 0.1d;
double j = h * i; // Double, not int- even if the answer is 1 in "normal" mathematics!
```
### Division and Integer Division:
Division is not so straightforward in Java. How division is played out depends entirely on the data types of the variables you are dividing. We'll start with division in integers first.

* **Integer Division** occurs when dividing a `byte`, `short`, `int`, or `long` with a `byte`, `short`, `int`, or `long`. For now, we'll just use `int`s for our examples. Integer division is unlike normal division in that we're only keeping the _quotient_ and discarding the _remainder_. 
* **Float Division** occurs when either the divident, or divisor, or both divident and divisor is a float.
Here's an example that shows the difference between integer division and float division in Java:
```Java
/* 
   Integer Division
   In normal math, 9/2 = 4 + 1/2. We get rid of the remainder, 1/2, for integer division.
*/
System.out.println(9 / 2); // 4
// Float Division
System.out.println(9.0 / 2.0); // 4.5
System.out.println(9.0 / 2); // 4.5
System.out.println(9 / 2.0); // 4.5
```
### Modulo:
Module is sort of like the opposite of integer division. Instead, we keep the _remainder_ and discard the _quotient_ for modulo. Modulo between two numbers is expressed like: `A % B`. This expression should return the remainder (in normal mathematics) for `A / B`.
```Java
/* 
   Modulo
   In normal math, 9/2 = 4 + 1/2. We get rid of the quotient, 4, for modulo.
*/
System.out.println(9 % 2); // 1.
```
### Scientific Notation in Java (Not So Important to Know):
**Reminder:** 
* Scientific notation allows us to multiple a number with a power of 10. It is a tool of convenience when writing large or small numbers.
 * For instance, it would be quite annoying to have to write `62700000000000` if we wanted. Instead, we can express this as 627 x 10<sup>11</sup>. (In true scientific notation, this would be 6.27 x 10<sup>13</sup>, but _who cares_?)
* Another way to write 627 x 10<sup>11</sup> is 627e11. This is how Java writes scientific notation as well.
Java allows scientific notation to be stored within `float` and `double`. Don't forget to add `f` and `d` at the end of variables!
Here's an example:
```Java
float scientific_one = 35e3f;
double scientific_two = 12e4d;
```
### Rounding Errors in Java:
While we humans easily can think of fractions and can think of numbers like 1/3 as 0.33333... with infinitely repeating 3's, that is not what Java (or other programming languages) do. Instead, Java uses 32-bit (4 bytes) or 64-bit (8 bytes) chunks of memory to store numbers. Therefore, Java has a limited number of spaces for decimals and often makes **rounding errors** by rounding numbers. `float` is especially bad with rounding errors because it is a 32-bit chunk of memory. While we will learn ways to combat rounding errors, we'll just use the `double` data type for now when we want to be more precise. `double` is more precise because it is a 64-bit chunk of memory.

## More Practice With Operations

```Java
// In the line below, declare two variables and multiply them together.

// In the line below, see if 232 is perfectly divisible by 3. If not, what is the remainder?

// In the line below, add a float to an integer and store that value.

// Bonus: In the line below, assign Avogadro's Number to a variable.

```
**Bonus Questions:** 
* Using modulo, how can you tell if an integer is even or odd?
* Using division, how can you tell if an integer is even or odd? 
  * (Hint: Think about integer division vs. float division.)
## Combining Libraries and Math | Using Java's Math Library:
If you've noticed, we have thus far excluded some of the essential operations that we use often in normal mathematics. Some of these include exponents (x to the power of y), special numbers like π, trigonometric functions like sin and cos, and the practice of rounding numbers. This is because there is no special operator like `+ - / * %` to do these. Instead, we use methods provided to us from Java's native `Math` library. (Native just means that it's built into Java).
### How to use the `Math` library:
* In order to use any of the methods from `Math`, import the math library by typing `import java.lang.Math;` before any class declarations.
### List of Commonly Used Math Methods and Variables:
**Assumption:** In the following methods, only numerical values are inputted.
* `Math.sqrt(x)`: Returns the square root of x as a `double`.
* `Math.pow(x, y)`: Returns x<sup>y</sup> as a `double`.
* `Math.sin(x)`: Returns sin x as a `double`.
* `Math.cos(x)`: Returns cos x as a `double`.
* `Math.tan(x)`: Returns tan x as a `double`.
* `Math.asin(x)`: Returns sin<sup>-1</sup> x as a `double`.
* `Math.acos(x)`: Returns cos<sup>-1</sup> x as a `double`.
* `Math.atan(x)`: Returns tan<sup>-1</sup> x as a `double`.
* `Math.exp(x)`: Returns e<sup>x</sup> as a `double`.
* `Math.log(x)`: Returns ln x as a `double`.
* `Math.log10(x)`: Returns log<sub>10</sub> x as a `double`.
* `Math.round(x)`: Rounds to nearest number. The result is an integer or a long, depending on the size of x.
* `Math.ceil(x)`: Rounds  up to nearest number. The result is a double.
* `Math.floor(x)`: Rounds down to nearest number. The result is a double.
* `Math.abs(x)`: Returns |x|. Returns number of the same data type as x.
* `Math.max(x, y)`: Returns y if x < y. Returns x if y < x.
* `Math.min(x, y)`: Returns x if x < y. Returns y if y < x.
Here's an example of some methods being used:
```Java
import java.lang.Math;
class MathTester {
  public static void main(String[] args) {
    System.out.println(Math.sqrt(9));
    System.out.println(Math.pow(2, 5));
    System.out.println(Math.round(3.5));
    System.out.println(Math.ceil(3.5));
    System.out.println(Math.floor(3.5));
    System.out.println(Math.min(3, 5.5));
  }
}
```
The output is:
```
3.0
32.0
4
4.0
3.0
3.0
```
### Order of Operations in Java:
**P**arentheses: They'll be our best friend in Java. We can't exactly write fractions, so we'll be using a lot of parentheses.
**F**unctions: Functions are executed next.
**M**ultiplication
**D**ivision
**A**ddition
**S**ubtraction
# Review
* Libraries allow for **reusability** of code.
* Integer division and modulo are complements to each other. While integer division finds quotients, modulo finds remainders.
* Math libraries help us perform more complicated mathematical operations.
* Storing numbers in the correcct data type is _essential_.
# Homework:
* Import the Math library in a Java class called `MathHomework.java`
* Is the square root of your age or half of your age smaller? Prove this using code.
  * Make sure to store the square root of your age in a variable.
  * Make sure to store half of your age in a variable. 
  * You'll need a function from the Math library that can return the smaller of two numbers. Store the result of this function.
  * Print out your answer.
* What will the _absolute_(no negative sign) age difference be between you and your mother when you're twice as old as you are now?
 * Hint: If you are _n_ years old today, you will be 2_n_ years old in _n_ more years. If she is _m_ years old today, your mother will be _m + n_ years old when you are _2n_ years old.
   * Store your age in _n_ years in a variable.
   * Store your mothers age in _n_ years in a variable.
   * Take the difference of these ages and store them in a variable.
   * Take the absolute value of this difference using a function and store it in a variable.
   * Print out your answer.
Here's an example for you to follow:
```Java
/*
Here's a Java program that will find the ages of my father and I when my father is twice as old as he is today.
*/
// Import Math
import java.lang.Math;
class MyDadIsOld {
  public static void main(String[] args) {
    System.out.println("Oh boy I have an old dad. Here goes nothing.");
    int myDadsAge = 43; // The age of an old, withered man.
    int myAge = 19; // The age of a fine specimen at the prime of his days and peak of his youth.
    int evenOlderDad = myDadsAge * 2; // Infinity times two.
    int aStillRelativelyYoungAge = myAge + myDadsAge; // I bet I still look great for my age.
    // I don't need to take the absolute value, but I'm just showing how Math.abs() works.
    int lookHowMuchYoungerIAm = Math.abs(evenOlderDad - aStillRelativelyYoungAge);
    System.out.println("My dad is this many years older than me:");
    System.out.println(lookHowMuchYoungerIAm);
    // Here is my age and my dad's age.
    System.out.println("My age today and in the future");
    System.out.println(myAge);
    System.out.println(aStillRelativelyYoungAge);
    System.out.println("My dad's age today and in the future");
    System.out.println(myDadsAge);
    System.out.println(evenOlderDad);
    // Just to confirm, let's see who will be younger both today and when my dad is ~even~ older.
    int smallerAge = Math.min(myAge, myDadsAge);
    System.out.println("I'm younger today:");
    System.out.println(smallerAge);
    int futureSmallerAge = Math.min(aStillRelativelyYoungAge, evenOlderDad);
    System.out.println("I'm younger in the future:");
    System.out.println(futureSmallerAge);
  }
}
```
Output:
```
Oh boy I have an old dad. Here goes nothing.
My dad is this many years older than me:
24
My age today and in the future
19
62
My dad's age today and in the future
43
86
I'm younger today:
19
I'm younger in the future:
62
```
