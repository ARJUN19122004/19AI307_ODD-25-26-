
---

# **Ex.No:5(D) THREAD PRIORITY**

## **QUESTION:**

Write a Java program to set the **priority** and **name** of two threads `t1` and `t2`.
Read the thread names from the user.
Set priority **4** for `t1` and **2** for `t2`.

---

## **AIM:**

To write a Java program that demonstrates **thread naming** and **thread priority assignment** using Java’s Thread class.

---

## **ALGORITHM:**

1. Start the program.
2. Import the necessary I/O classes.
3. Read two thread names from the user using `BufferedReader`.
4. Create two thread objects `t1` and `t2`.
5. Set names for both threads using `setName()`.
6. Set the priority of `t1` to **4** and `t2` to **2**.
7. Display their details using `toString()`.
8. End the program.

---

## **PROGRAM:**

```
/*
Program to implement a Thread Priority Concept using Java
Developed by: 
RegisterNumber:  
*/
```

---

## **SOURCE CODE:**

```java
import java.io.*;

public class Main {
    public static void main(String[] args) throws Exception {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

        // Read thread names from user
        String name1 = br.readLine().trim();
        String name2 = br.readLine().trim();

        // Create threads
        Thread t1 = new Thread();
        t1.setName(name1);
        t1.setPriority(4);

        Thread t2 = new Thread();
        t2.setName(name2);
        t2.setPriority(2);

        // Print thread details
        System.out.println(t1.toString());
        System.out.println(t2.toString());
    }
}
```

---

## **OUTPUT:**

<img width="789" height="237" alt="image" src="https://github.com/user-attachments/assets/470609cd-f57f-4ed3-bbf1-2c58cb7e5dfd" />


---

## **RESULT:**

Thus, the Java program to set **thread names** and **thread priorities** for `t1` and `t2` was successfully executed.

---

