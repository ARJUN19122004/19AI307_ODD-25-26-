

---

# **Ex.No:4(A) EXCEPTION HANDLING**

## **QUESTION:**

You wrote a program that stores input strings into a String array and prints each string in uppercase.
However, you're getting a **NullPointerException**.
**What should you check in your array before calling `.toUpperCase()` on an element?**

---

## **AIM:**

To implement exception handling in Java and prevent `NullPointerException` by checking array elements before using string methods.

---

## **ALGORITHM :**

1. Start the program.
2. Import the package `java.util`.
3. Read multiple string inputs from the user.
4. Store them into a dynamic list and convert the list into an array.
5. Traverse the array.
6. **Before calling `.toUpperCase()`**, check whether the element is:

   * `null`, or
   * the literal string `"null"`.
7. If null → print **"Null element"**.
8. Else → convert to uppercase and print.
9. End the program.

---

## **PROGRAM:**

```
/*
Program to implement Exception Handling using Java
Developed by:
RegisterNumber:
*/
```

---

## **SOURCE CODE:**

```java
import java.util.*;

public class UppercaseStrings {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Read input lines until a blank line
        List<String> list = new ArrayList<>();
        while (sc.hasNextLine()) {
            String input = sc.nextLine().trim();
            if (input.isEmpty()) break;
            list.add(input);
        }

        String[] arr = list.toArray(new String[0]);

        // Print each string in uppercase with null checks
        for (String str : arr) {
            if (str == null || str.equalsIgnoreCase("null")) {
                System.out.println("Null element");
            } else {
                System.out.println(str.toUpperCase());
            }
        }

        sc.close();
    }
}
```

---

## **OUTPUT:**

```
<img width="514" height="252" alt="image" src="https://github.com/user-attachments/assets/e23dfb9a-a170-4c2a-9f7f-346588f92ac6" />


```

---

## **RESULT:**

Thus, the program was successfully executed using **exception handling** concepts.

---



