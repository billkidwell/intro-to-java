# Variables and Types

One of the first things we need to understand are *variables*.

Variables store data.  Since Java is a strongly-typed language, each variable also has a *type*.

## String

Let's start with *String*.  Strings store text, and are surrounded by double quotes.

You have to *declare* a variable.  This starts with providing the type, the name, and can also include a value.


This declares a variable of type String, with the name firstName.
```java
String firstName;
```

For variable names, we use *lowerCamelCase*.  The variable starts with a lower case letter, but each additional word in the variable name gets an upper case letter. It is called Camel Case, because each upper case letter is a hump on the camel's back.

This is a convention, which means the compiler won't enforce this, but it makes it easier for us to read.  We need to REMEMBER this.

## Assigning a value

We can assign values to a variable with the assignment operator (the equal sign)

```java
firstName = "Steve";
```

Notice that for assignment, we use the single =.  Like most statements in Java, it ends with a semi colon.  You can change the value of the variable with another assignment operator. 

Let's try it out.

[NameCaller](https://www.online-java.com/COHiAXvASd)

### Exercise:
Update the example to add your name!

If we wanted to, we could assign the value when we declare the variable.  For example, 

```java
String firstName = "Steve";
```

### Exercise:
Try changing the example so that "Steve" is assigned when the variable is declared, and remove the line where we assign the value "Steve" to the variable.

## char
The char type stores a single character.  You assign a character by providing the value in single quotes.

```java
char grade = 'B';
System.out.println("The student's grade is " + grade);
```
Most of the time, we will want to use a String, but sometimes it makes more sense to work with individual characters.

## Integers
Integers are whole numbers without decimals.  They can be positive or negative.  

Examples:

- 123

- -123

We declare an integer with *int*.

```java
int length = 10;
```

Now, we can have the program do some math! 

You probably remember that you get the area of a rectangle by multiplying the length by the width.  In Java, we multiply with the * operator.  

```java
int length = 10;
int width = 6;
int area;

// Calculate ate area of the rectangle
area = length * width;

System.out.println("The rectangle is " + length + " long and " + width + " wide.");
System.out.println("The area of the rectangle is " + area);
```

There are shortcuts for declating multiple variables of the same type.  For example:

```java
int length = 10, width = 6, area;
```

This works because they are all integers.
This can make it harder to find your variable later, so use it when the variables are very similar to each other. 

## Boolean

A boolean variable is true or false.  They are named after the famous mathematician, George Boole, who defined Boolean algebra. 

A boolean variable is declared like other variables.

```java
boolean isAdult = false;
```

We will learn more about boolean logic in a future class.

## Other types

Here is a table that describes other *primitive* data types in Java.

| Data Type | Description |
| --- | --- |
| byte | Stores whole numbers from -128 to 128 |
| short | Stores whole numbers from -32,768 to 32,767 |
| int | Stores whole numbers from -2,147,483,648 to 2,147,483,647 |
| long | Stores really large whole numbers |
| float | Stores fractional numbers with 6 to 7 decimal digits |
| double | Stores fractional numbers with 15 to 16 decimal digits |
| boolean | Stores true or false values |
| char | Stores a single character |

Note that *String* is not a primitive type.  You can tell by the capital letter S in the front.  It is a class.  It manages a collection of characters. It is important enough that we are covering it early. 

## An exercise

Let's put what we have learned to the test.  Use the following link to complete this assignment.

```java
public class Main {
  public static void main(String[] args) {
    // Declare a string that holds a student's name here
    // Declare a variable to hold the student's grade level (1-12) here.
    // Declare a variable to hold the student's score (A, B, C, D, F) here.

    // Print the student's name
    // Print the student's grade level
    // Print the student's grade
  }
}
```
[Link to assignment](https://www.online-java.com/cf5R28Q9hm)

