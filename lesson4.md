---
tags: [Java101]
title: lesson4
created: '2019-08-07T13:23:06.953Z'
modified: '2019-08-07T13:53:55.355Z'
---

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
### Creating a Class and Class Variables:
Let's make this concrete with an example:
![Alt text](car_blueprint.jpg)
* If classes are the Java equivalent of blueprints, let's make a class called `CarModel` that represents a car.
  * When designing a class, we need to give the class attributes. We'll give the car the following attributes:
    * The name of the driver.
    * The year the car was built.
    * The price of the car
```Java
public class CarModel {
    String driverName;
    int carYear;
    double carPrice;
}
```
### Creating a constructor:
Now, in order to really turn this class into  blueprint, we'll need to make a constructor. Constructors are guidelines on how to turn a generic class into an object. Below is the syntax for two constructors:

To make this a more concrete example:
```Java
public class CarModel {
    // These are variables that are attributes of the CarModel class.
    String driverName;
    int carYear;
    double carPrice;
    // This is a default constructor.
    public CarModel() {
        // Nothing is assigned here. driverName, carYear, and carPrice will be null, 0, and 0.0 by default.
    }
    
    // This is not a default constructor. This will modify the attributes of this class when creating an object.
    public CarModel(String driverNameArgument, int carYearArgument, double carPriceArgument) {
        driverName = driverNameArgument;
        carYear = carYearArgument;
        carPrice = carPriceArgument;
    }
}
```
### Using a constructor:
Now that we've made the constructors- the blueprint- we need to make an actual instance of a class- an object. The syntax for creating an object using a constructor is the following:
`ClassName objName = new ClassName();`. 
* The `ClassName` before `objName` tells Java that the variable `objName` will be an instance of the class `ClassName`.
* The `new` keyword tells Java that a brand new place in memory must be reserved for a `new` object that will be a `ClassName` object.
* `ClassName()` is a call to a **Constructor**. A constructor is a block of code that creates an instance of a class. Typically, class attributes are assigned within the constructor.
  * If a constructor does not accept any arguments, this is called a **default constructor**. This creates a generic form of your object.
  * If a constructor accept arguments, then the attributes of the object will change based on the arguments passed into the constructor.
```Java
public class CarModel {
    // These are variables that are attributes of the CarModel class.
    String driverName;
    int carYear;
    double carPrice;
    // This is a default constructor.
    public CarModel() {
        // Nothing is assigned here. driverName, carYear, and carPrice will be null, 0, and 0.0 by default.
    }
    
    // This is not a default constructor. This will modify the attributes of this class when creating an object.
    public CarModel(String driverNameArgument, int carYearArgument, double carPriceArgument) {
        driverName = driverNameArgument;
        carYear = carYearArgument;
        carPrice = carPriceArgument;
    }
    // If the main method is a to-do list, let's make put making a CarModel object on our "list".
    public static void main(String[] args) {
        // Let's start with a default constructor.
        CarModel genericCar = new CarModel();
        /*  
            To retrieve an attribute of an object, we use objectName.attributeName.
            We'll be printing the attributes of the genericCar object using System.out.println().
            Let's test out the attributes of this car:
        */
        System.out.println(genericCar.driverName);
        System.out.println(genericCar.carYear);
        System.out.println(genericCar.carPrice);
        // Let's use the other constructor. First, we'll declare variables to use later.
        String myName = "Furkan";
        int myCarYear = 2014;
        double myCarWorth = 10000;
        /* Now let's input these variables as the arguments into the constructor.
           It's important to input the arguments in the order stated in the constructor.
           If there is a mismatch between the order of data types, there will be an error.
           For example, this constructor expects a String, an int, and a double.
        */
        CarModel myCar = new CarModel(myName, myCarYear, myCarWorth); 
        System.out.println(myCar.driverName);
        System.out.println(myCar.carYear);
        System.out.println(myCar.carPrice);
    }
}
```
# Review:
* Java is an object orientated programming language.
* Classes represent concepts.
* Objects are instances of classes.
* You need a constructor to create an object from a class.
* You can access attributes using the following syntax: `objName.attributeName`
# Homework
Create a `Student` class. Make it a default constructor and a second constructor. Make sure it has at least 3 class variables. Display the object's attributes once you're done using `System.out.println()`.
