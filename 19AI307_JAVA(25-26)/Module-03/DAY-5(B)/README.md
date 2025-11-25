
---

# **Ex.No:3(F) WRAPPER CLASS**

## **QUESTION:**

Write a Java program that uses the **Boolean wrapper class** in conditional logic to determine a **Pass/Fail** result.

---

## **AIM:**

To write a Java program using the **Boolean wrapper class** and apply it in conditional statements.

---

## **ALGORITHM :**

1. Start the program.
2. Import the package **java.util.Scanner**.
3. Read input marks from the user.
4. Use the **Boolean wrapper class** to store pass/fail condition.
5. Check the Boolean value using an `if` condition.
6. Display **"Pass"** if true, else display **"Fail"**.
7. End the program.

---

## **PROGRAM:**

```
/*
Program to implement a Wrapper Class using Java
Developed by: 
RegisterNumber:  
*/
```

---

## **SOURCE CODE:**

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int marks = sc.nextInt();

        // Using Boolean wrapper class
        Boolean isPass = marks >= 50;

        if (isPass) {
            System.out.println("Result: Pass");
        } else {
            System.out.println("Result: Fail");
        }

        sc.close();
    }
}
```

---

## **OUTPUT:**


<img width="426" height="251" alt="image" src="https://github.com/user-attachments/assets/f80f33f1-d76c-47b5-8877-96b14c79063f" />


---

## **RESULT:**

Thus, the Java program using the **Boolean Wrapper Class** to determine Pass/Fail was successfully executed.

---

