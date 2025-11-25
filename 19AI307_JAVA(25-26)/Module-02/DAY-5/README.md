
---

# **Ex.No:2(E) ACCESS MODIFIERS**

## **QUESTION:**

Write a method that accepts a string and returns whether it contains only lowercase letters or not.

---

## **AIM:**

To write a Java program that uses access modifiers and implements a method to check whether a given string contains only lowercase characters.

---

## **ALGORITHM :**

1. Start the program.
2. Import the package `java.util`.
3. Create a method to check if all characters in a string are lowercase.
4. Traverse each character using a loop.
5. If any character is not lowercase, return false.
6. Otherwise, return true.
7. In the `main()` method, read input and call the method.
8. Display the result.
9. End the program.

---

## **PROGRAM:**

```java
/*
Program to implement Access Modifiers using Java
Developed by: Arjun M
RegisterNumber: 212222040012
*/
```

---

## **SOURCE CODE:**

```java
import java.util.Scanner;

class prog {

    public static boolean isAllLowercase(String input) {
        for (char c : input.toCharArray()) {
            if (!Character.isLowerCase(c)) {
                return false;
            }
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String str = scanner.nextLine();

        boolean r = isAllLowercase(str);
        System.out.println(r);
    }
}
```

---

## **OUTPUT:**
<img width="356" height="241" alt="image" src="https://github.com/user-attachments/assets/7fd9a731-e5e6-466c-b693-52ec54769101" />

---

## **RESULT:**

Thus, the Java program using access modifiers to check if a string contains only lowercase letters was executed successfully.

---
