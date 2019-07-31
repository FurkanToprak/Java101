# Java 101 | Lesson 3:
## Variables:
In computer science, **variable** is a name for a place in memory that can store values. Let's take a look at the diagram below.
<br>
![alt text](memory.png)
<br>
Above, you can see a portion of memory with a predetermined size storing the number `5`. The variable, or portion of allocated memory, that is capable of storing numbers is called `a` in the diagram above. Appropriately named, `variables` can vary. `a` can just as easily contain any value, as long as it can store it within the size of its allocated memory.
If we wanted to make a variable with name `a` and value `5` in java, all it would require would be:
```Java
int a = 5;
```
If we wanted to read this out, we would say _integer a is assigned 5_. Here's how the above line works:
* `int` is a **data type** (reviewed next section) that lets our program know that we'll be storing a whole number within a.
* `a` is the **variable name**. All this does is **allocate** a portion of memory and name it `a`.
* `=` is the **assignment operator**. The assignment operator assigns the _value_ on the right side of the operator to the variable on the left side of the operator.

## Data Types:
Earlier, we mentioned that `a` had a _predetermined_ size. This means that the program knows how much memory to allocate to variable `a` before trying to store a value. How did the program know how much memory to allocate?
We specified `a`'s data type as an `int`. `int` is one of the many data types. Let's review some data types:
* Data types can be separated as **primitive** or **non-primitive**. For now, all you need to know that primitive data types are all lowercase whereas non-primitive data types are capitalized.
### Primitive Data Types:
* `int`: The **integer** data type can store whole numbers that do not contain decimal points.
  * Let's say you wanted to make an app that stored a user's grades. If you wanted to store the number of courses the user is taking, you would store it within an `int` object because courses are counted with whole numbers (you can't take 0.23 of a class!).
```Java
int courseNumber = 7;
```
* `double`: The **double** data type can store numbers that contain decimal points.
  * If you wanted to store the numerical grade that the user had in a class, you would use a double.
```Java
double mathAverage = 89.3;
```
* `char`: The **character** data type can store single characters that are within the [Unicode Standard](https://en.wikipedia.org/wiki/Unicode). Unicode is the global standard for text in software.
  * If you wanted to store the letter grade for one of the courses the user is taking you would use a `char`. Because letter grades can only be displayed as `A`, `B`, `C`, `D`, or `F`, it makes sense to store it within a `char` variable.
  * When assigning a character, be sure to encapsulate the specific character in single quotations. 
  * Whether a character is capital or not matters! In Java, `'A'` and `'a'` are different `char`s!
```Java
double mathLetter = 'A';
```
* `boolean`: The **Boolean** data type can store only two values, `true` or `false`.
  * If you wanted to know if the user is passing all of their classes, you would use a boolean. This is because you can only pass or fail a class. In other words, your passing status can only be `true` or `false`. 
```Java
boolean isPassing = true;
```
* `byte`, `short`, `float`, and `long`: These data types are used for storing numbers in more technical ways. You don't need to know anything about them for now.
### Non-primitive Data Types:
## Math in Java:
