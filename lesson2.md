# Java 101 | Lesson 2:
## Understanding Java Syntax:
We'll be starting from the most general concepts to the most specific concepts. 
### Java Files:
Java source code files end with the `.java` extension. When the code is _compiled_, it produces a program with the same name but `.class` extension. This is called a **bytecode** file. A bytecode file is binary (1's and 0's) code executable by a **Java Virtual Machine (JVM)**. The JVM enables computers to run Java programs that are compiled as bytecode. For a `.java` source code to be able to be compiled, there needs to be no _syntax errors_. Syntax errors are mistakes we make when we don't follow coding conventions for Java. These conventions are important for the _Compiler_ to be able to turn our source code into bytecode.
* You can compile program through your IDE.
  * To compile and run in Eclipse, follow [this guide](http://pages.cs.wisc.edu/~cs302/labs/EclipseTutorial/Step_04.html).
  * To compile and run in NetBeans, follow [this guide](https://netbeans.org/kb/docs/java/quickstart.html#run).
  
We'll be constructing a file called `HelloWorld.java`. This will produce a file called `HelloWorld.class` when compiled.
### Classes:
Let's build a Java file from scratch.
```Java
public class HelloWorld {

}
```
Classes are one of the broadest concepts in Java, but think of them as a single _object_ that accomplishes a general task. All this bit of code accomplishes thus far is it _declares_ a class named HelloWorld. Everything that we'll put within the curly braces will be contained within the domain of the HelloWorld class.
### The `main()` method:
Let's add a _method_ in the class. A method is a single block of code that achieves the same purpose. This method will be called `main()`. The `main()` method lists the things the program achieves. We'll be adding things for the program to achieve in a bit.
```Java
public class HelloWorld {
    public static void main(String[] args) {
    }
}
```
We'll learn what `public`, `static`, and `void` mean later. Also ignore the stuff within the paranthesis. We'll get to all of that in time.
### Printing:
If we want to display a message, we have to use _print_ statements. Print statements tell the program to _output_ certain information. Let's add a print statement.
```Java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
This line of code prints out `Hello, World!` to the terminal. You may be wondering about the odd-looking statement needed to print something (`System.out.println`), but all you need to do for now is know that any `argument` we put within the parenthesis and surround with quotations will be printed out to the terminal.
<br><br>**Notes**:
* If you'll notice, this looks different than the previous code. This line of code does not have any curly braces and ends with a semicolon. Every line of code in Java (other than methods, classes, and a couple other exceptions) ends with `;`. This syntax tells our interpreter that a line of code or specific instruction has ended.
* By now, you might have noticed that we indent code after every curly brace. This is to organize our code and is called **indentation**. Please keep in mind that each indentation is four spaces or one tab in Java. Please pick one of the two and consistently use it. It doesn't matter which one you pick as long as you're consistent.
### Comments
Often times, it's useful to annotate your code. In order to be able to make comments about your code, without affecting the rest of the code, we put either use single- or multi- line comments.
#### Single-line comments:
Let's say we wanted to add a comment to the previous code- maybe information about what the code does. If we can fit this information on a single line, we'll just add `//` right before our comment. Here's an example:
```Java
// This is a class
public class HelloWorld {
    // This is the main method.
    public static void main(String[] args) {
        // This is a print statement. Make sure to allign your comments so that they are indented with the rest of the code.
        System.out.println("Hello, World!"); // We can also put comments right after a line of code, like this.
    }
}
```
#### Multi-line comments:
Maybe single-line comments aren't cutting it for you. Let's say you'd like to write a comment that won't fit on a single line. For this, you need to encapsulate your multi-line comment like this:
```Java
public class HelloWorld {
    /*
    This is how multi-line comments work.
    Don't forget to indent the comment at the same level.
    It's also bad programming practice to have comments that exceed the 100'th column on a single line.
    For example, the previous line had exceeded to the 103rd column.
    */
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
## Naming conventions:
* Classes always start with a capital letter. Every word within the class has a capital first letter. For example, `HelloWorld` is capitalized at the beginning of every new word. This is called **CamelCase**.
* Classes, methods, and variables (we'll learn about them later- let this just be for future reference) should not start with an underscore, dollar sign, capital letter, or number.
* **Important:** In Java, names for methods, classes, and variables *cannot* contain spaces or punctuation marks (`-`, `,`, `+`, etc) in them. See the first bullet point for multi-worded class names. For variables names with multiple words, words should either be separated with underscores or the words after the first word should start with a capital letter.
* Constants (we'll learn about them later) should be in all capital letters, and multiple words should be separated by underscores. 
Here are some examples of good and bad naming convention:
```Java
// Classes should be CamelCased.
public class GoodConvention {
    // Remember to indent! 4 spaces or a tab!
    // Good variable name
    int someNumber;
    int some_number;
    // Bad variable name
    // These are just bad naming convention: it will still run but is bad naming convention.
    int SomeNumber;
    int somenumber;
    int SOMENUMBER;
    // These bad names are so bad that Java doesn't know what this means! The program will not compile.
    int 1number;
    int some number;
    int _someNumber;
    int $someNumber;
}
```

## Review:
* Java source code is in `.java` files and is compiled into `.class` bytecode files.
* A class represents a general concept that a program achieves.
* The `main()` method acts as a checklist of things for a class to do.
* We can print by using `System.out.println()`.
* Curly braces encapsulate smaller chunks of code within a scope.
* Semicolons are put at the end of statements.
* Comments are useful for annotating code.
* White spaces help us read code easily.
* Syntax is the name given to the collection of rules followed for the compiler to be able to read code and convert it into bytecode. Good syntax is also really useful for humans to read code.
* There are naming conventions of classes, methods, variables, and constants. These should be followed, or the program may not compile, do something we didn't intend, or 

## Homework:
Compile and run a program that prints out: `I did my homework, Furkan!`.
