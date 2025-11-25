
---

# **Ex.No:5(A) INPUTSTREAMREADER**

## **QUESTION:**

Write a Java program to read characters from the keyboard using **InputStreamReader**.

---

## **AIM:**

To write a Java program that uses **InputStreamReader** to read characters from the user and display the output.

---

## **ALGORITHM :**

1. Start the program.
2. Import the necessary I/O classes.
3. Create an `InputStreamReader` object to read bytes and convert them into characters.
4. Read characters from the keyboard using `read()`.
5. Stop reading when the user enters a termination character.
6. Display the entered characters.
7. End the program.

---

## **PROGRAM:**

```
/*
Program to implement InputStreamReader using Java
Developed by: Arjun M
Register Number: 212222040012
*/
```

---

## **SOURCE CODE:**

```java
import java.io.InputStreamReader;
import java.io.IOException;

public class InputReaderDemo {
    public static void main(String[] args) throws IOException {
        InputStreamReader isr = new InputStreamReader(System.in);

        System.out.println("Enter characters (press '0' to stop):");

        char ch;
        do {
            ch = (char) isr.read();
            System.out.print(ch);
        } while (ch != '0');
    }
}
```

---

## **OUTPUT:**

<img width="829" height="321" alt="image" src="https://github.com/user-attachments/assets/2d122860-5dc6-4ffa-8c16-87e94d083726" />


---

## **RESULT:**

Thus, the program to implement **InputStreamReader** in Java was executed successfully.

---
