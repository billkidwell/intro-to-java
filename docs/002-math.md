# Math and Operators

As you might expect, Java provides a lot of ways to perform calculations.  Let's start with common Arithmetic (math) operators. 

## Arithmetic Operators

| operation | operator | example |
| --- | --- | --- |
| add | + | int sum = 100 + 50; // 150 |
| subtract | - | int difference = 100 - 50; // 50 |
| multiply | * | int product = 100 * 50; // 5000 |
| division | / | int quotient = 100 / 50; // 2 |
| modulus | % | int remainder = 3 % 2; // 1 |

## Increment and Decrement Operators
It is very common to increase an integer value by 1, or to decrease an integer value by 1.  It is so common, that there are shortcuts.

| operation | operator | example | long format | 
| --- | --- | --- | --- |
| increment | ++ | ++x | x = x + 1 |
| decrement | -- | --x | x = x - 1 |

## Exercise - Sharing cookies
Let's put this to work in an example.  

In this example, you will fill in some missing code. We want to keep track of the number of friends that we have in the room.  We start with 2.  Three friends enter and one leaves. 

Then, we want to divide up the cookies.  They may not divide evenly, so there may be some cookies left over.  

```java
public class Main {
  public static void main(String[] args) {
    
    int numCookies = 24;
    int numFriends = 2;
    
    System.out.println("Friends in the room - " + numFriends);
    
    // write code to show that 3 friends entered the room
    
    
    // write code to show that 1 friend left the room
    
    System.out.println("Final number of friends - " + numFriends);
    
    // Calculate the number of cookies per person in the room
    // Add the resulting variable to the print statement below
    System.out.println("Number of cookies per friend - ");
    
    // Calculate the number of cookies remaining 
    // Add the resulting variable to the print statement below
    System.out.println("Number of cookies remaining - " );
  }
}
```
[Exercise](https://www.online-java.com/f6glVCmtRj)

