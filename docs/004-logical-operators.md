# Logical Operators

A lot of programming involves using logic to determine what actions happen. 

There are three logic operators that we care about. Let's start with the simplest. 

## NOT !

The Logical not returns the opposite of its argument.  "Not True" is false, and "Not False" is true.

We can show this in a truth table

| value | !value |
| --- | --- |
| true | false |
| false | true |

## AND &&

If you have two logic values, you can combine them with the AND operator.  This will return true if both values are true. 

Q = A && B

| A | B | Q |
| --- | --- | --- |
| false | false | false |
| true | false | false |
| false | true | false |
| **true** | **true** | **true** |

## OR || 

You can also combine two values with the OR operator.  This will return true if either A or B is true.

Q = A || B

| A | B | Q |
| --- | --- | --- |
| false | false | false |
| **true** | **false** | **true** |
| **false** | **true** | **true** |
| **true** | **true** | **true** |

## An example

Here is an example of how you can use logic to create rules in a Java program.  Let's write a small Java program to determine if a person is allowed to watch an "R-Rated" movie.  Here are the rules

* A person can enter if they are 18 or older.
* If they are under 18, they can still enter if they have a parent with them. 
* Regardless of age, they cannot enter if they have been banned fromm the theater.

```java
public class MovieTheater {
    public static void main(String[] args) {
        int age = 16;
        boolean hasParent = true;
        boolean isBanned = false;

        boolean canEnter = (!isBanned) && (age >= 18 || hasParent);

        if (canEnter) {
            System.out.println("Enjoy the movie!");
        } else {
            System.out.println("Access denied.");
        }
    }
}
```

Let's look at different scenariosl with this code.

* age = 20, hasParent = false, isBanned = false
  * They are 18 and Not banned, so they can enter
  * Result: Allowed
* age = 15, hasParent = false, isBanned = false
  * They are under 18 and don't have a parent with them
  * Result: Denied
* age = 25, hasParent = false, isBanned = true
  * They are banned, so they cannot enter regardless of age
  * Result: Denied

## Home Alarm Exercise

[Exercise](https://www.online-java.com/BPo6183Yp3)

Try this exercise.

```java
/**
 * Goal: Create a program that decides if the house alarm should sound.
 * 
 * Rules:
 * 1. The alarm sounds if a motion sensor is triggered 
 *    while the system is armed.
 * 2. If the emergency button is pressed, the alarm 
 *    sounds immediately (regardless of whether it is armed).
 * 3. If the maintenance mode is active, the alarm never sounds, 
 *    even if motion is detected or the emergency button is pressed.
 */
public class HomeSecurity {
    public static void main(String[] args) {
    boolean isArmed = true;
        boolean motionDetected = true;
        boolean emergencyButtonPressed = false;
        boolean maintenanceMode = false;

        // TASK: Replace false with the logic for the home alarm using &&, ||, and !
        boolean isAlarmRinging = false;

        System.out.println("Alarm sounding: " + isAlarmRinging);        
    }
}
```