---
title: While Loop
---
# While Loop

while loop is most basic loop in Java. It has one control condition, and executes as long the condition is true. The condition of the loop is tested before the body of the loop is executed, hence it is called an entry-controlled loop.

The basic format of while loop statement is:

Syntax:
```java
While (condition)
{
   statement(s);
   Incrementation;
}
```

The `while` loop executes a group of statements until an expression evaluates to `true`. For instance:

```java
while (some_condition_is_true)
{
    // do something
}
```

**Note**: For the `while` loop to start executing, you'd require the condition to be true. However, to exit the loop you must do something as given below (otherwise the loop will execute forever. Practically, it will run till the JVM runs out of memory).

## Example
In the following example, the `expression` is given by `iter_While < 10`. As we increment `iter_While` by `1` each time the loop is executed, the `while` loop will keep going until `iter_While` reaches `10`.

```java
int iter_While = 0;
while (iter_While < 10)
{
    System.out.print(iter_While + " ");
    // Increment the counter
    // Iterated 10 times, iter_While 0,1,2...9
    iter_While++;
}
System.out.println("iter_While Value: " + iter_While);
```

Output:
```
0 1 2 3 4 5 6 7 8 9
iter_While Value: 10
```

![:rocket:](//forum.freecodecamp.com/images/emoji/emoji_one/rocket.png?v=2 ":rocket:") <a href='https://repl.it/CJYj/0' target='_blank' rel='nofollow'>Run Code</a>
