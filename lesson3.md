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
Earlier, we mentioned that `a` had a _predetermined_ size. This means that the program knows how much memory to allocate to variable `a` before trying to store a value.
## Math in Java:
