
---

# Ex.No:1(C) LOOPING STATEMENT

## **QUESTION:**

Write a Java program to calculate the factorial of a number using a **for loop**.

---

## **AIM:**

To write a Java program that reads a number from the user and computes its factorial using looping statements.

---

## **ALGORITHM :**

1. Start the program.
2. Import the necessary package `java.util`.
3. Read an integer input from the user.
4. Initialize a variable `f = 1` to store the factorial.
5. Use a **for loop** from 1 to the given number.
6. Multiply the loop counter value with `f` in each iteration.
7. Print the final computed factorial.
8. End the program.

---

## **PROGRAM:**

```java
/*
Program to implement a Looping Statement using Java
Developed by: Arjun M
RegisterNumber: 212222040012
*/
```

---

## **SOURCE CODE:**

```java
import java.util.*;

class prog {
    public static void main(String[] args)
    {
        int f = 1;
        int a;

        Scanner sc = new Scanner(System.in);
        a = sc.nextInt();

        for (int i = 1; i <= a; i++) {
            f = f * i;
        }

        System.out.println("Factorial of " + a + " is: " + f);
    }
}
```

---

## **OUTPUT:**

<img width="704" height="246" alt="image" src="https://github.com/user-attachments/assets/39220182-1247-4670-990c-d9edeb8195cb" />






---

## **RESULT:**

Thus, the Java program using looping statements to calculate the factorial of a number was executed successfully.

---


