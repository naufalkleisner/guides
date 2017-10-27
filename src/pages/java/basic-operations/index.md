---
title: Basic Operations
---
# Basic Operations

Java supports the following operations on variables:

*   Arithmetic : `Addition(+)`, `Subtraction(-)`, `Multiplication(*)`, `Division(/)`, `Modulus(%)`,`Increment(++)`,`Decrement(--)`.
*   String concatenation: `+` can be used for String concatenation but subtraction `-` on a String is not a valid operation.
*   Relational: `Equal to(==)`, `Not Equal to (!=)`, `Greater than(>)`, `Less than(<)`, `Greater than or equal to(>=)`, `Less than or equal to(<=)`
*   Bitwise: `Bitwise And(&)`, `Bitwise Or(|)`, `Bitwise XOR(^)`, `Bitwise Compliment(~)`, `Left shift(<<)`, `Right Shift (>>)`, `Zero fill right shift (>>>)`
*   Logical: `Logical And (&&)`, `Logical Or(||)`, `Logical Not (!)`
*   Assignment: `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `<<=`, `>>=`, `&=`, `^=`, `|=`
*   Others: `Conditional/Ternary(?:)`, `instanceof`

While most of the operations are self-explanatory, the Conditional (Ternary) Operator works as follows:

`expression that results in boolean output ? return this value if true : return this value if false`

For e.g:
```java
    int x = 10;
    int y = (x == 10) ? 5 : 9; // y will equal 5 since the expression x == 10 evaluates to true
   
```

Assignment Operators

Operator	Description

*   =	Assign
*   +=	Increments, then assigns
*   -=	Decrements, then assigns
*   *=	Multiplies, then assigns
*   /=	Divides, then assigns
*   %=	Modulus, then assigns
*   <<=	Left shift and assigns
*   >>=	Right shift and assigns
*   &=	Bitwise AND assigns
*   ^=	Bitwise exclusive OR and assigns
*   |=	Bitwise inclusive OR and assigns


Programs to Show How Assignment Operator Works

```java
Example:
import java.util.*;
import java.lang.*;
import java.io.*;

public class arithop {
 public static void main(String[] args) {
  int number1 = 6;
  int number2 = 8;
  int sum = number1 + number2;
  int dif = number1 - number2;
  int mul = number1 * number2;
  int quot = number1 / number2;
  int rem = number1 % number2;
  
  System.out.println("number1 is : " + number1);
  System.out.println("number2 is: " + number2);
  System.out.println("Sum is: " + sum);
  System.out.println("Difference is : " + dif);
  System.out.println("Multiplied value is : " + mul);
  System.out.println("Quotient is : " + quot);
  System.out.println("Remainder is : " + rem);
 }
}
```
