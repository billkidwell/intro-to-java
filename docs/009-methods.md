# Methods in Java

Methods, also known as functions, are blocks of code that we can call.  You can also pass information, through parameters, to a method.  

Methods make it easier to reuse code.  They also make code easier to read. 

## A simple method

We have already been working with the `main` method in Java.  Let's expand that to include our own methods. 

```java

public class Main {

    static void sayHello() {
        System.out.println("Hello!");
    }
    
    public static void main(String[] args) {
        sayHello();
    }

}

```

As you can see in this example, we create a method called `sayHello`.  This uses camel casing as the naming convention.  The first letter is lower case.  The first letter of each new word is upper case.  

We don't provide an access modifier (like `public` or `protected`) so it defaults to `private`.  We wouldn't be able to call this method from another class.  

This method is `static` because it is a class method.  You don't have to create an object to call the class.  We will learn more about this when we talk about creating classes and objects. 

The `void` keyword means that this method does not return any data. 

The empty parentheses mean that we aren't passing any parameters. 

In main, we are calling the `sayHello` method.  Basically, we can take the block of code inside `sayHello` and substitute it in `main`.  

## Passing values to our method

Now, let's expand our example with parameters.  Let's add a new version of `sayHello` that accepts a name.  

```java
static void sayHello(String firstName) {
    System.out.println("Hello " + firstName + "!");
}
```

Now, we can call this with different values.  `firstName` is our *parameter* and the values that we pass in, e.g. "Xander" and "Trent" are *arguments*.

```java
public static void main(String[] args) {
    sayHello("Xander");
    sayHello("Trent");
}
```

## Return values

What if we want our method to return a value?  Let's write a method that returns the remainder.  The modulus operator (`%`) does this, but it can be easy to forget. 

Recall that when we divide two numbers, the first number is called the *dividend* and the second is the *divisor*;

```java
static int getRemainder(int dividend, int divisor) {
    return dividend % divisor;
}
```

We see that we no longer have `void` as a return type, and we replaced it with `int`.  We expect this method to return an `int` value. 

You can also see that we declare two parameters for our function.  Each of them is an `int`.  We separate them with a `,`.

To call this, we could do the following:

```java
int remainder = getRemainder(5, 2);
```

After this call, `remainder` is equal to `1`.

## Method overloading

Sometimes, we need a method that can take different types of values.  When we use the same name, but different parameters, we call this **method overloading**.  

A simple example would be an `add` method. We don't really need one, since we can just use `+`, but let's write one to see how this works. 

```java
public class Main {
    static int add(int a, int b) {
        System.out.println("Adding integers!");
        return a + b;
    }

    static double add(double a, double b) {
        System.out.println("Adding doubles!");
        return a + b;
    }

    public static void main(String[] args) {
        int intAnswer = add(5, 3);
        System.out.println("Answer is " + intAnswer);

        double doubleAnswer = add(5.1, 3.1);
        System.out.println("Answer is " + doubleAnswer);
    }
}
```

When you run this code, you get the following output:

```
Adding integers!
Answer is 8
Adding doubles!
Answer is 8.2
```

[Try it here](https://www.online-java.com/V31SiZ0bOr)

Can you trace the code and see why it prints that output?

### Let's put this into practice.  

```java
public class Main {
    
    static String[] months = {
        "January", 
        "February", 
        "March", 
        "April", 
        "May",
        "June", 
        "July", 
        "August",
        "September", 
        "October", 
        "November",
        "December"
    };
    
    /**
     * Take a number from 1-12 and return the month name.  Use the months array. 
     * 
     * HINT: indexes start at zero.  Try subtracting 1
     */
    static String getMonthName(int monthNumber) {
        // Change this to return the month name from the array.
        return "";
    }
    
    /**
     * This function should return "Winter" for December, January, or February.
     * It should return "Spring" for March, April or May.
     * It should return "Summer" for June, July, or August.
     * It should return "Fall" for September, October or November.
     */
    static String getSeasonName(int monthNumber) {
        String season = "Unknown";
        
        // Add your code here to turn the number into the 
        // appropriate string.  You can use a switch statement, or an if-else
        
        return season;
    }
    

    public static void main(String[] args) {
        
        int month = 2; 
        String monthName = getMonthName(month);
        System.out.println("Month Number: " + month);
        System.out.println("Month name: " + monthName);
        
        String seasonName = getSeasonName(month);
        System.out.println("Season: " + seasonName);
    }
}
```

[Month methods](https://www.online-java.com/JczLtNLdDB)

For bonus points, change the main method so that it loops from 1-12 and prints the names and seasons for all of the months.

