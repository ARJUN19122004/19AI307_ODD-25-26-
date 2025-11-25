
---

# **Ex.No:5(C) FILE HANDLING USING JAVA**

## **QUESTION:**

Write a Java program to read multiple lines from the user (or a file-like input) and **reverse the order of words in each line**.

---

## **AIM:**

To implement file handling in Java using `BufferedReader` and perform text processing by reversing the words in each input line.

---

## **ALGORITHM:**

1. Start the program.
2. Import required packages (`java.io.*`, `java.util.*`).
3. Create a `BufferedReader` to read input line by line.
4. Keep reading lines until the user enters `"exit"`.
5. For each line, split the words using space.
6. Reverse the order of words.
7. Print the reversed output.
8. End the program.

---

## **PROGRAM:**

```
/*
Program to implement File Handling using Java
Developed by: 
RegisterNumber:  
*/
```

---

## **SOURCE CODE:**

```java
import java.io.*;
import java.util.*;

public class Main {
    public static void main(String[] args) throws Exception {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        List<String> lines = new ArrayList<>();
        String line;

        // Read lines until 'exit'
        while ((line = br.readLine()) != null) {
            if (line.equalsIgnoreCase("exit"))
                break;
            lines.add(line);
        }

        System.out.println("Reversed lines:");

        // Reverse words in each line
        for (String l : lines) {
            String[] words = l.trim().split("\\s+");
            StringBuilder sb = new StringBuilder();

            for (int i = words.length - 1; i >= 0; i--) {
                sb.append(words[i]);
                if (i != 0) sb.append(" ");
            }

            System.out.println(sb.toString());
        }
    }
}
```

---

## **OUTPUT:**

<img width="836" height="318" alt="image" src="https://github.com/user-attachments/assets/d026aedd-7d1d-470e-be0e-8d061820b0eb" />


---

## **RESULT:**

Thus, the Java program for **File Handling** using `BufferedReader` to reverse the order of words in each line was successfully executed.

---


