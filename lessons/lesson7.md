# Java 101 | Lesson 7:
## User input
Sometimes in a program, some user input is required. For this, we need a scanner. The `Scanner` object is not readily available, however, so we need to import it from the `java.util` package- shown below:

```
import java.util.Scanner;
class InputTester {
    public static void main(String[] args) {
        // System.in is a stream in Java that represents user input.
        Scanner userInput = new Scanner(System.in);
    }
}
```
Using the scanner, we can ask the user to give us many forms of input, with the following methods:
* nextBoolean()
* nextByte()
* nextDouble()
* nextFloat()	
* nextInt()
* nextLine()
* nextLong()
* nextShort()

Here are some examples: 

```
import java.util.Scanner;
class InputTester {
    public static void main(String[] args) {
        // System.in is a stream in Java that represents user input.
        Scanner userInput = new Scanner(System.in);
        int userAge = userInput.nextInt();
        String userName = userInput.nextString();
    }
}
```
## String Concatenation
In Java, strings and variables can be combined in order to make for more interesting output.
```java
class ConcatExample {
    public static void main(String[] args) {
        String a = "string1";
        String b = "string2";
        // Equivalent to "string1string2"
        String c = a + b;
        // We can also combine other sorts of variables, as long as the object type has a .toString() method.
        // Equivalent to string15
        String d = a + 5;
    }
}
```
There is nearly no end to the possibilities of String concatenation. Feel free to search around for more thorough examples of string concatenation.