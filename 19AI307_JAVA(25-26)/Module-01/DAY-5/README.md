
---

# **Ex.No:1(E) STRINGS AND MATH FUNCTION**

## **QUESTION:**

Write a Java program to compare two strings.

---

## **AIM:**

To write a Java program that reads two strings from the user and compares them using the `equals()` method of the String class.

---

## **ALGORITHM :**

1. Start the program.
2. Import the package `java.util`.
3. Create a `Scanner` object to read input.
4. Read the first string.
5. Read the second string.
6. Compare the two strings using `equals()`.
7. If both are equal, display: **"Strings are equal."**
8. Otherwise, display: **"Strings are not equal."**
9. End the program.

---

## **PROGRAM:**

```java
/*
Program to implement Strings and Math Function using Java
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
        Scanner sc = new Scanner(System.in);

        String s = sc.nextLine();
        String st = sc.nextLine();

        if (s.equals(st)) {
            System.out.println("Strings are equal.");
        }
        else {
            System.out.println("Strings are not equal.");
        }
    }
}
```

---

## **OUTPUT:**

<img width="647" height="314" alt="image" src="https://github.com/user-attachments/assets/2bcc259b-cc99-45a9-9ffa-dc1afd595e1e" />



## **RESULT:**

Thus, the Java program to compare two strings using the `equals()` method was executed successfully.

---


