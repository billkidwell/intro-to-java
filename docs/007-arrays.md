# Arrays

In Java, an array is a way to store multiple values, like a list.

You declare an array by defining a variable type with square brackets [ ]

```java
String[] cars; // declare an array of String values called `cars`
```

You can provide an initial list of values in the declaration by including a comma-separated list inside curly braces { }.

```java
String[] cars = {"Ford", "Subaru", "Volkswagen"};
```

## Accessing the elements of an array

You can access the elements of an array by referring to the index number.  

The first index is zero.  

```java
String[] cars = {"Ford", "Subaru", "Volkswagen"};
System.out.println(cars[0]); // Ford
System.out.println(cars[1]); // Subaru
System.out.println(cars[2]); // Volkswagen
```

## Getting the size of an array

You can get the size of the array using the `length` property.

```java
String[] cars = {"Ford", "Subaru", "Volkswagen"};
System.out.println(cars.length); // 3
```

### Exercise

Let's combine our knowledge of arrays with our knowledge of while loops.

Write a java program that loops through an array and prints the values at each index.

[Exercise](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

[Click here to try again](https://www.online-java.com/61BicaWCel)



