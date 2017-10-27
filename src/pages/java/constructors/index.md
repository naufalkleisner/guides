---
title: Constructors
---
# Constructors

What are Constructors?


Constructors are special member functions whose task is to initialize the objects of its class. It is treated as a special member function because its name is the same as the class name. Java constructors are invoked when their objects are created. It is named such because, it constructs the value i.e. provide data for the object, i.e. they are used to initialize objects. Every class has a constructor, when we don’t explicitly declare a constructor for any java class the compiler creates a default constructor for that class which does not have any return type. Constructor in Java cannot be abstract, static, final or synchronized and these modifiers are not allowed for constructor.




What's the point then? I should be able to store data in it right?

That's when we use either **getter** (e.g., getName()) / **setter** (e.g., setName()) methods or in this case constructors to initialize a class. Basically every Java Class has a constructor, which is the method which is called first when any object of the class is initialized. Think of it as a bit of starter code.

Characteristics of Java Constructors

*   Interface cannot have constructor.
*   Constructors cannot be private.
*   A constructor cannot be abstract, static, final, native, strictfp, or synchronized
*   A constructor can be overloaded.
*   Constructors cannot return a value.
*   Constructors do not have a return type; not even void.
*   Abstract class can have constructor.
*   Constructors name must be similar to that of class name inside which it resides.
*   Constructors are automatically called when an object is created.

 Instance variables and methods of a class are known as members of a class. Constructors are not members. For this reason, constructors cannot be inherited; but can be accessed by a subclass. Actually, Java constructors do not get inherited; only their members (variables and methods) get inherited. So declaring a constructor as final is useless and has no meaning as constructors cannot be overridden. Again, Java constructors should not be synchronized as it locks the object when created and hence, as long as the object is not created no other object can be instantiated.

When you write a class without any constructor, then Java assumes it has a default constructor :

```java
public class Car {
    private String name;
}

Car modelS = new Car();
```

This initializing with no parameters is a way of calling the default constructor. You can also have a default constructor written yourself this way :

```java
public class Car {
    private String name;

    public Car() {
        name = "Tesla";
    }
}
```

Then, when calling `new Car()`, the variable `name` will get auto-initialized to `"Tesla"`.

Clearly, constructors are exactly what they sound like: they are used to `construct` i.e., instantiate an object of a particular class.  
Constructors look similar to method declarations, but are slightly different in the sense that they:

1.  Are named exactly the same as the class.
2.  Don't have a return type.

Hence, the purpose of using `constructors` is to provide:

1.  A way to instantiate an object.
2.  Provide initial values to a object properties.
3.  Control how an object is created.

Let's look at another example. Say, Honda (the car manufacturer), wants all its cars to be named `Honda <something>`. In order to enforce this, we might represent this using a class as follows:

```java
public class Car {

    private String name;

    //Constructor.
    public Car(String model){
        this.name = "Honda " + model;
    }

    public String getName(){
        return this.name;
    }

    public static void main(String args[]){
        Car car = new Car("Civic");
        System.out.println( car.getName() );
    }
}
```

![:rocket:](//forum.freecodecamp.com/images/emoji/emoji_one/rocket.png?v=2 ":rocket:") <a href='https://repl.it/CTJ4/1' target='_blank' rel='nofollow'>Run Code</a>

Notice that when we write a constructor in this way i.e., providing a parameter, we are `controlling` (point no. 3) the way an instance of `Car` is created. In short, we are saying in this example that `you MUST provide a model name in order to get an instance of Car class`.

Why is this important? There are times when you'd want `one and only one` instance of a class which you'd want to use in your entire application. One way of achieving this is by using a `private` constructor.

Assume you need a class to represent a Bank. You wouldn't want people to create instance of `Bank` ever. So, you design your class:

```java
public class Bank {

    private static Bank instance;
    
    private Bank(){
    }

    public static Bank getInstance(){
        if(null == instance){
            instance = new Bank();
        }
        return instance;
    }
}
```

![:rocket:](//forum.freecodecamp.com/images/emoji/emoji_one/rocket.png?v=2 ":rocket:") <a href='https://repl.it/CTJz/0' target='_blank' rel='nofollow'>Run Code</a>

Notice that the constructor is `private`. This enforces the fact that no one else is allowed to create an `instance` of the Bank.  
In fact, if in another class, you try:

```java
Bank account = new Bank(); //-> throws a compilation error: Bank() has private access in Bank.
```

So, the only way to gain access to the instance is by using `Bank.getInstance()`. Such instances are called `Singleton` since you get exactly one instance (per VM to be precise) throughout the life of your application.


There can be many number of constructors in a class. But they should differ in the method parameters. This is Constructor Overloading. For example

```java
public class Car {

    private String name;
    private String carType;

    //Constructor.
    public Car(){
        this.name = "No Name";
        this.carType = "No Type";
    }
    public Car(String model){
        this.name = "Honda " + model;
    }
    
    public Car(String model, String carType){
        this.name = model;
        this.carType = carType;
    }
    
    public String getName(){
        return this.name;
    }
    
    public String getCarType(){
        return this.name;
    }

    public static void main(String args[]){
        Car car = new Car("Civic");
        System.out.println( car.getName() );
        
        //Other Way To Initialize
        Car car = new Car("Civic","Sedan");
        System.out.println( car.getName() + " "+ car.getCarType() );
        
    }
}

```
