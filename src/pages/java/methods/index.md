---
title: Methods
---
# Methods

There are certain rules that a programmer should follow in order to implement overriding. These are:

*   In java, a method can only be written in child class and not in same class.
*   Argument list should be exactly the same as that of the overridden method of that class.
*   Instance methods can also be overridden if they are inherited by the child class.
*   A constructor cannot be overridden.
*   Final – declared methods cannot be overridden.
*   Any method that is static cannot be used to override.
*   The return type must have to be the same or a subtype of the return type declared in the original overridden method in the parent class.
*   If a method cannot be inherited then it cannot be overridden.
*   A child class within the same package as the instance’s parent class can override any parent class method that is not declared private or final.
*   A child class in a different package can only override the non-final methods declared as public or protected.

`getName()` and `getManufacturerName()` are two "Getter" methods we have used here. Notice, unlike JavaScript, we **have** to define the return type of any method we write, otherwise it will fail at compile time. If you do not want a method to return anything, use `void` return type.

```java
public class Car {
    private String name;

    public void changeName() {
        name = "Tesla";
    }
}
```
Example:

```java

class college {
 public void move() {
  System.out.println("College is open");
 }
}
class univ extends college {
 public void move() {
  System.out.println("University is open too");
 }
}
public class stud {
 public static void main(String args[]) {
  college a = new college();
  college b = new univ();
  a.move();
  b.move();
 }
}
```
As with any other language, methods (or functions, if you are here from JS world) are used often for their modularity and reusability.
