# Java 101 | Lesson 4
## Introduction:
Java is an **object-orientated** language. This means that **everything in Java is either a class, an instance of a class (an object), or an attribute of a class or object.**
## Classes:
A class is a blueprint for creating an object. Because everything is either an object or object-related in Java, every Java file we've written so far start with a class declaration.<br>
**SomeClass.java:**
```Java
public class SomeClass
{
}
```
## Objects:
An object is an instance of a class. If a class is a blueprint of a concept, an object is the implementation of the blueprint itself. Here's how to write an object within a class:
**SomeClass.java:**
```Java
public class SomeClass
{
    public static void main(String[] args) {
        // We've just made our first object!
        SomeClass someObject = new SomeClass();
    }
}
```
All that is required to make an object of a certain class is to write
```Java
ClassName objectVariable = new ClassName();
```
Now, `objectVariable` is an instance of `ClassName`. Any property that `ClassName` has, `objectVariable` will as well.
## Combining the Concepts:
Let's make this concrete with an example:
![Alt text](car_blueprint.jpg)
* If classes are the Java equivalent of blueprints, let's make a class called `CarModel` that represents a car.
  * When designing a class, we need to give the class attributes. Let's 
