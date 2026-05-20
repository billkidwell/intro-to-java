# While loops

Loops are common in software programs.  The while loop is the most common type.  Most other loops can be written as while loops.

What does a while loop look like?

It consists of the `while` keyword, a condition, and a code block that we want repeated.

```java
while (condition) {
    // code block to be executed
}
```

One thing that doesn't show here, though.  Whenever we create a loop, we need to think about the stop condition.  

Let's look at an example.

```java
int num = 0;

while (num < 3) {
    System.out.println(num);
    num++;
}
```

In this example, we start with `num` with a value of zero.  Let's walk through each iteration of the loop.

| num |  description |
| --- | --- |
| 0 | In the first iteration, num == 0 which is less than 3, so we print 0 and increase num. |
| 1 | On the second iteration, num == 1 which is still less than 3, so we print 1 and increase num by one |
| 2 | On the third iteration, num == 2 which is still less than 3, so we print 2 and increase num by one |
| 3 | Now, num == 3.  Since num is no longer less than 3, we skip the code block and exit the loop. |

### Question time

* What would happen if we never increased num?  
* What would happen if we decreased it instead of increasing it?

### Exercise

Write a program that will countdown from 10, printing a number on each line. After the countdown, print "Blast Off!"

[Exercise](https://www.online-java.com/2BPq4EQJvD)

```java
public class Countdown {
    public static void main(String[] args) {
        
        int num = 10;
        
        // Use a while loop to countdown from to 10 to zero.
        
        System.out.println("Blast Off!");

    }
}
```

