# Classes

Java is an object-oriented programming language.  Java is about creating objects with data and methods. 

But what is a class?

Think of class as in "classification".  We define a class, for example, `Car`.  When we create objects of type `Car`, they get their own identities, and include details like specific models 'Subaru', 'Ford', 'Volkswagen".  Or a class `Fruit` might result in 'Apple', 'Banana', and 'Pear'.  Just like a class `Student` might have objects 'Xander' and 'Trent'

> A class is like a blueprint for the object we want to create.

A class can have data called **attributes**.  These are just variables that belong to the class.

This example class has a name attribute of type String.

```java
public class Student {
    String name;
}
```

Since we don't specify, the variable name is `private`.  That means that I can't access it outside of the class `Student`.  

We generally like to add "getters" and "setters" to control access.

```java
public class Student {
    String name;

    public void setName(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }
}
```

> Notice how we use `this.name` to differentiate the `name` that belongs to the class from the `name` that is an argument.

## Creating Objects

Now that we have created a class, let's use it to create some objects.

```java
public class Main {
    
    public static void main(String[] args) {
        
        // Create a new object - xander
        Student xander = new Student();
        xander.setName("Xander");
        
        Student trent = new Student();
        trent.setName("Trent");
        
    }
}
```

Now we have some `Student` objects (also called instances).  Notice how we use the `new` operator to create them. 

We can improve our class by giving it a custom `constructor`.  Constructors are a special kind of method that are used during creation. 

What if we provided the name of the `Student` object when we created it?

This constructor is public.  It needs to be in order to be called outside of our class.  Notice that there is no return type, and the name of the constructor is the class name.  

We define one argument, `name`, which we will use to set the name of the Student during creation.

```java
    public Student(String name) {
        this.setName(name);
    }

```

Now, our previous example looks like this:

```java
        Student xander = new Student("Xander");
        Student trent = new Student("Trent");
```

Very nice!

## toString()

How do we get a String representation of our object?

Objects have a built-in method called toString().  If we print an object, it calls this method.

```java
        System.out.println(xander);
        System.out.println(trent);
```

This prints something like this:

```
Student@76ed5528
Student@2c7b84de
```

That's not super helpful.  It is telling us that those are objects of class `Student` at those addresses in memory.  However, we can make our own `toString` method!

```
    public String toString() {
        return "Student: " + name;
    }
```

Now when we call the code above, we get this:

```
Student: Xander
Student: Trent
```

## Exercise: Add Age

Let's take this Student example, and add the following

1) Add a new attribute, age, that takes an integer

2) Add a new setter and getter for age

3) Update our toString feature to output the age, like this:

    `Student: Xander, Age: 12`
    
4) Update main to set the student's ages

    ```
    xander.setAge(12);
    trent.setAge(10);
    ```

[Exercise](https://www.online-java.com/1FIxm8Q2nt)
