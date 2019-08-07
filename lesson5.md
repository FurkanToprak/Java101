---
tags: [Java101]
title: lesson5
created: '2019-08-07T13:23:06.953Z'
modified: '2019-08-07T14:45:33.955Z'
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

### Modulo:

### Rounding Errors in Java:
### Order of Operations in Java:
## Combining Libraries and Math | Using Java's Math Library:
```Java
import Java.lang.Math;
```
### Scientific Numbers:
Java allows scientific notation to be stored within `float` and `double`. Don't forget to add `f` and `d` at the end of variables!
Here's an example:
```Java
float scientific_one = 35e3f;
double scientific_two = 12E4d;
```
