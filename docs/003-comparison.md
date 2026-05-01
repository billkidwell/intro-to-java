# Comparison

When you have variables with different values, you often need to compare them to decide what your program should do. 

In this section we talk about comparison operators.  These result in a value of true or false. 

## Equal ==

One tricky thing to remember is that when comparing two values, you use ==, when assigning a value, you use =;

```java
int x = 5;
System.out.println(x == 5); // returns true
```

## Additional comparison operators

This table provides more examples of comparison operators that you may need.

| operator | description | example |
| --- | --- | --- |
| == | Equal to | x == 5 |
| != | Not equal | x != 5 |
| > | Greater than | x > 5 |
| < | Less than | x < 5 |
| >= | Greater than or equal to | x >= 5 |
| <= | Less than or equal to | x <= 5 |

We will see later that ! is used for NOT. That should help us remember !=.  I still remember greater than and less than operators based on the fact that the opening is toward the larger number, like the jaws of an alligator gobbling up the larger number. 

\>= and <= are shortcuts.  It is very common that you want to know if something is equal to a boundary, or greater than that boundary.  These operators prevent us from typing both conditions. 

As an example, someone is considered a legal adult if they are 18 years of age, or older.
```java
boolean isAdult = age >= 18;
```
## Exercise: The Roller Coaster Gate

Imagine you are building a digital gate for a theme park ride called The Dragon Helper. The ride has height rules to keep everyone safe.

Your Tasks
* Fill in the correct equations to determine if the rider is tall enough. 
* Test the program with these values for height:
    * Try 40, 48, 50, 72 and 73

The program does the following
* If height is 48 or taller, it prints: "You are tall enough to ride!"
* If height is less than 48, it prints: "Sorry, you are too short for this ride."
* A special bonus check inside prints: "Wow, you are a giant! Sit in the front row." if the rider is exactly 72 inches.

[Try it Now](https://www.online-java.com/3HWv2EtKBE)

```java
public class Main {
    public static void main(String[] args) {
        int height = 50; // Try 40, 48, 72 and 73!

        // replace the values here with the correct conditions
        // For example `boolean aboveFreezing = temperature > 32; ``
        boolean tallEnough = false;
        boolean isGiant = false;
        
        // You should not need to change anything below this line

        if (tallEnough) {
            if (isGiant) {
                System.out.println("Wow, you are a giant! Sit in the front row.");
            } else {
                System.out.println("You are tall enough to ride!");
            }
        } else {
            System.out.println("Sorry, you are too short for this ride.");
        }
    }
}

```