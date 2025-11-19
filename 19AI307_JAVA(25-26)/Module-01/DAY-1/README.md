---

# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## **QUESTION:**

Write a Java program to demonstrate the use of variables and different operators.

---

## **AIM:**

To write a Java program that uses different assignment, arithmetic, bitwise, and shift operators to modify a value step by step.

---

## **ALGORITHM :**

1. Start the program.
2. Read an integer input from the user.
3. Apply various assignment operators such as +=, -=, *=, /=, %=.
4. Apply bitwise operators |=, &=, ^=.
5. Apply shift operators <<= and >>=.
6. Display the result after each step.
7. Print the final output.
8. End the program.

---

## **PROGRAM:**

```java
/*
Program to implement Variables and Operators using Java
Developed by: 
Register Number: 
*/

import java.util.*;

class prog {
    public static void main(String[] main)
    {
        int a;
        Scanner sc = new Scanner(System.in);

        a = sc.nextInt();
        System.out.println("Initial Power = " + a);

        a += 5;
        System.out.println("After Door 1 (+= 5): " + a);

        a -= 3;
        System.out.println("After Door 2 (-= 3): " + a);

        a *= 2;
        System.out.println("After Door 3 (*= 2): " + a);

        a /= 4;
        System.out.println("After Door 4 (/= 4): " + a);

        a %= 3;
        System.out.println("After Door 5 (%= 3): " + a);

        a |= 2;
        System.out.println("After Door 6 (|= 2): " + a);

        a &= 7;
        System.out.println("After Door 7 (&= 7): " + a);

        a ^= 4;
        System.out.println("After Door 8 (^= 4): " + a);

        a <<= 1;
        System.out.println("After Door 9 (<<= 1): " + a);

        a >>= 1;
        System.out.println("After Door 10 (>>= 1): " + a);

        System.out.println("Final Power = " + a);

        sc.close();
    }
}
```

---

## **OUTPUT:**


<img width="637" height="366" alt="image" src="https://github.com/user-attachments/assets/0eb3c118-643c-4092-ba1c-ba53a62bf7ab" />

---

## **RESULT:**

Thus, the Java program to demonstrate variables and different types of operators was executed successfully.

---


