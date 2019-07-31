# Java 101 | Lesson 2:
## Understanding Java Syntax:
We'll be starting from the most general concepts to the most specific concepts. 
### Java Files:
Java source code files end with the `.java` extension. When the code is _compiled_, it produces a program with the same name but `.class` extension. This is called a **bytecode** file. A bytecode file is binary (1's and 0's) code executable by a **Java Virtual Machine (JVM)**. The JVM enables computers to run Java programs that are compiled as bytecode.
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
**Notes**:
* If you'll notice, this looks different than the previous code. This line of code does not have any curly braces and ends with a semicolon. Every line of code in Java (other than methods, classes, and a couple other exceptions) ends with `;`. This syntax tells our interpreter that a line of code or specific instruction has ended.
* By now, you might have noticed that we indent code after every curly brace. This is to organize our code. Please keep in mind that each indentation is four spaces or one tab. Please pick one of the two and consistently use it. It doesn't matter which one you pick as long as you're consistent.
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

