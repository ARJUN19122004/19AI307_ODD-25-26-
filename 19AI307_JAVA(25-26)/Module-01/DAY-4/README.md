
---

# Ex.No:1(D) ARRAYS

## **QUESTION:**

Write a Java program to count how many elements in an array are divisible by **3 or 5**.

---

## **AIM:**

To write a Java program that reads an array of integers and counts how many elements are divisible by 3 or 5 using array concepts.

---

## **ALGORITHM :**

1. Start the program.
2. Import the necessary package `java.util`.
3. Read the size of the array from the user.
4. Declare an integer array of the given size.
5. Read all elements of the array using a loop.
6. Check each element:

   * If it is divisible by 3 **or** 5, increase the counter.
7. Print the count.
8. End the program.

---

## **PROGRAM:**

```java
/*
Program to implement an Array concept using Java
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
        int n;
        Scanner sc = new Scanner(System.in);

        n = sc.nextInt();            // size of array
        int arr[] = new int[n];     // array declaration
        int c = 0;                  // counter

        for (int i = 0; i < n; i++)
        {
            arr[i] = sc.nextInt();

            if (arr[i] % 3 == 0 || arr[i] % 5 == 0)
            {
                c++;
            }
        }

        System.out.println(c);
    }
}
```

---

## **OUTPUT:**

<img width="351" height="324" alt="image" src="https://github.com/user-attachments/assets/88f309f7-b77c-4b99-9d82-5ac831edbff4" />


## **RESULT:**

Thus, the Java program using arrays to count elements divisible by 3 or 5 was executed successfully.

---


