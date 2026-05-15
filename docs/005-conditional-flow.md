# Conditional flow

When we talk about the flow of a program, we are talking about which parts of the code run, and which parts are skipped.  In this section, let's learn a few different ways we can control the flow of a program.  We have already used some of these in prior exercises.

## if

An if statement specifies a **block of code** that should be executed if a condition is true.

```java
if (condition) {
    // block of code to be executed if the condition is true
}
```

We can use boolean variables and comparison operators to make this very readable.

```java
int height = 72; 
boolean isTallEnough = height > 48;

if (isTallEnough) {
    System.out.println("Enjoy the ride");
}
```

### Beware the missing { }
Our curly brackets define the block of code associated with our `if` statement.  If you leave them off, the block of code the next statement.

```java
int height = 72; 
boolean isTallEnough = height > 48;

if (isTallEnough) 
    System.out.println("Enjoy the ride");
```
This works the same way as the example above.  However, it is best to use the curly brackets.  There is a common mistake in this code... can you find it?

```java
int height = 40; 
boolean isTallEnough = height > 48;

if (isTallEnough) 
    System.out.println("Buckle your seatbelt.");
    System.out.println("Enjoy the ride!");
```

Try this code and see if you can spot the error.

[Enjoy the ride](https://www.online-java.com/PcS1QtpOSe)

## if ... else

Often, we also need to do something if the condition is not true.  To do this, we can use the if ... else ... structure.

```java
if (condition) {
    // block of code to be executed if the condition is true
} else {
    // block of code to be executed if the condition is false
}
```

Let's revisit our example that looked at heights. We can use the if ... else ... to take an action based on whether a person is tall enough for our carnival ride.

```java
int height = 72; 
boolean isTallEnough = height > 48;

if (isTallEnough) {
    System.out.println("You are tall enough to ride!");
} else {
    System.out.println("Sorry, you are too short for this ride.");
}
```

## if ... else if ... else ...

We don't have to stop there, though.  We can evaluate multiple conditions. 

```java
if (condition) {
    // block of code to be executed if the condition is true
} else if (anotherCondition) {
    // block of code to be executed if the condition is false 
    // and anotherCondition is true
} else {
    // block of code to be executed if the condition is false
    // and anotherCondition if false
}
```
Notice here, first we check `condition`.  If it is true, we don't even check `anotherCondition`.  We know what to do.  If it is false, then we continue, and we evaluate `anotherCondition`. 

```java
int height = 72; 

if (height > 72) {
    System.out.println("You are a giant!");
} else if (height > 48) {
    System.out.println("You are tall enough to ride!");
} else {
    System.out.println("Sorry, you are too short for this ride.");
}
```

Let's evaluate this for different values of height.  Can you fill in the other values?

| height | output |
| --- | --- |
| 74 | You are a giant! |
| 72 | |
| 50 | |
| 48 | |
| 47 | |

## Nested if ...

What if we wanted to print "You are a giant! You are tall enough to ride!" in the case where the user was over 72 inches?  We can put if statements inside of if statements.  This is called a **nested** if statement.

```java
int height = 72; 

if (height > 48) {
    if (height > 72) {
        System.out.print("You are a giant! ");
    }
    System.out.println("You are tall enough to ride!");
} else {
    System.out.println("Sorry, you are too short for this ride.");
}
```
With this code, If `height` is greater than 48, the computer will move to line 98 and evaluate that if statement.  If `height` is greater than 72, it will execute the block that prints "You are a giant! ".  Either way, it will execute the line 101 and output "You are tall enought to ride!".

## Exercise

Let's write a Grade Calculator.  Scores are often a percentage (0 - 100) and there is a grade table that translates the numeric score to a grade letter.  

Here is a table that is often used:

| Percentage Score | Letter Grade |
| --- | --- |
| 90 - 100 | A |
| 80 - 89 | B |
| 70 - 79 | C |
| 60 - 69 | D |
| 0 - 59 | F |

Let's write a grade calculator that will output the correct letter grade. 

[Grade Calculator](https://www.online-java.com/u0Yim6op1I)
