# More Loops

The while loop is the most basic way to control loops in our software.  However, there are other varieties.  In a lot of cases, they are better because they help us prevent common errors. 

## For Loop

The `for` loop is commonly used when we have a counter that controls a loop.  The basic synax looks like this:

```java
for (statement 1; statement 2; statement 3) {
  // code block to be executed
}
```

statement 1 initializes the loop.

statement 2 is the stop condition for the loop.

statement 3 is executed after the code block.  It is usually used to increment or decrement a counter.

Let's look at one of our previous examples:

```java
int num = 0;

while (num < 3) {
    System.out.println(num);
    num++;
}
```

We can rewrite this using a for loop.

```java
for (int num = 0; num < 3; num++) {
    System.out.println(num);
}
```
In this version, all of the statements thtat control the loop are in the `for` line.  

What if we wanted to do something more interesting, like provide all even numbers between 0 and 10? 

```java
for (int num = 0; num <= 10; num = num +2) {
    System.out.println(num);
}
```

In this example, we increment `num` by 2 each time, so we only get the even numbers.  We use `<=10` so we should get 0, 2, 4, 6, 8 and 10 in our output.

### Exercise: Count by Tens

[Exercise](https://www.online-java.com/4PUw1InHtk)

```java
public class Main {
    public static void main(String[] args) {
        
        // Use a for loop to count from 0 to 100 by 10s.
    }
}
```

### Exercise: Multiplication Tables

With that exercise working, let's try something more advanced.  Let's use the computer to print part of our multiplication tables.  Given a number, write a loop that will show the multipleication table column for that number (0-12). 

For example, if we give the number 3, print out the following:

```
Multiplication table
3 x 0 = 0
3 x 1 = 3
3 x 2 = 6
3 x 3 = 9
3 x 4 = 12
3 x 5 = 15
3 x 6 = 18
3 x 7 = 21
3 x 8 = 24
3 x 9 = 27
3 x 10 = 30
3 x 11 = 33
3 x 12 = 36
```

[Exercise](https://www.online-java.com/VHgJhx8syq)

```java
public class Main {
    public static void main(String[] args) {
        
        int num = 3;
        
        System.out.println("Multiplication table");
        
        // Use a for loop to print out the multiplication table for num
        
    }
}
```

## For-Each Loop

Another version of the for loop is very helpful for working with arrays.   

A for-each loop looks like this:

```java
for (type variableName : arrayName) {
  // code block to be executed
}
```

Here is an example of printing all of the cars from our last lesson.

```java
String[] cars = {"Ford", "Subaru", "Volkswagen"};
for (String car: cars) {
    System.out.println(car);
}
```

Notice that we create a variable named `car` of type `String`.  The current value from the array `cars` will be assigned to that variable, and we can use it in the code block.  On the next iteration of the array, the next value will be assigned.  

The variable `car` does not exist outside of our block of code for the for-each loop.  It is `scoped` to that code block.

```java
       String[] cars = {"Ford", "Subaru", "Volkswagen"};
        for (String car: cars) {
            System.out.println(car);
        }
        System.out.println(car); // causes an error!
```

What if we had an array of `int`?  The variable in the for-each loop has to be compatible with the array.  

```java
    int[] evens = {0, 2, 4, 6, 8, 10};

    for (int num : evens) {
        System.out.println(num);
    }
```

### Exercise: Never Gonna Give You Up... again

Let's update our code for Never Gonna Give You Up to use a for-each loop.

[Exercise](https://www.online-java.com/pZQvKOVojj)

```java
public class Countdown {
    public static void main(String[] args) {
        
        String[] thingsIWillNeverDo = {
            "give you up",
            "let you down",
            "run around and desert you",
            "make you cry",
            "say goodbye",
            "tell a lie and hurt you"
        };
        
        // Use a for-each loop to print the lyrics 
        // to Never Gonna Give You Up
        // For bonus points, repeat the lyrics three types.  
        // Separate each group with a blank line.
    }
}
```

