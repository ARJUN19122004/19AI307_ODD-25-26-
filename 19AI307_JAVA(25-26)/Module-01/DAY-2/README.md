

# Ex.No:1(B) CONDITIONAL STATEMENT

## **QUESTION:**

Write a Java program to simulate an elevator with magical behavior based on conditional statements.

---

## **AIM:**

To write a Java program that takes a floor number as input and displays messages based on divisibility conditions using conditional statements.

---

## **ALGORITHM :**

1. Start the program.
2. Import the necessary package `java.util`.
3. Read the floor number from the user.
4. Check if the number is divisible by both 3 and 5 → print **"Skipped"**.
5. Else if divisible by 3 → print **"Beware!"**.
6. Else if divisible by 5 → print **"Blessings!"**.
7. Otherwise → print **"Floor {number}"**.
8. Stop the program.

---

## **PROGRAM:**

```java
/*
Program to implement a conditional statement using Java
Developed by: Arjun M
RegisterNumber: 212222040012
*/
```

---

## **SOURCE CODE:**

```java
import java.util.*;

class prog {
    public static void main(String [] args)
    {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();

        if (a % 3 == 0 && a % 5 == 0) {
            System.out.println("Skipped");
        }
        else if (a % 3 == 0) {
            System.out.println("Beware!");
        }
        else if (a % 5 == 0) {
            System.out.println("Blessings!");
        }
        else {
            System.out.println("Floor " + a);
        }
    }
}
```

---

## **OUTPUT:**

<img width="461" height="300" alt="image" src="https://github.com/user-attachments/assets/e57957f5-aaa5-4d61-9d42-c4090c723cba" />



---

## **RESULT:**

Thus, the Java program using conditional statements to simulate a magical elevator was executed successfully.

---

If you want **Ex.No:2 – Looping Statements** next in GitHub format, tell me!
