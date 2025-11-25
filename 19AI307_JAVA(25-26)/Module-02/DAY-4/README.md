
---

# **Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR**

## **QUESTION:**

Create a class **Student** with private instance variables and a constructor to initialize them.

---

## **AIM:**

To understand variable scope and implement constructors in Java by creating a class with private attributes and initializing them using a constructor.

---

## **ALGORITHM :**

1. Start the program.
2. Import the package `java.util`.
3. Create a class `Student` with private variables: ID, Name, and Age.
4. Define a constructor to initialize these variables.
5. Define a method to display the student details.
6. In the `main()` method, read user inputs and create a `Student` object.
7. Call the display method to print the details.
8. End the program.

---

## **PROGRAM:**

```java
/*
Program to implement Variable Scope and Constructor using Java
Developed by: Arjun M
RegisterNumber: 212222040012
*/
```

---

## **SOURCE CODE:**

```java
import java.util.*;

class prog {
    private int studentID;
    private String studentName;
    private int studentAge;

    public prog(int id, String name, int age) {
        this.studentID = id;
        this.studentName = name;
        this.studentAge = age;
    }

    public void display() {
        System.out.println("Student Details: ");
        System.out.println("Student ID: " + studentID);
        System.out.println("Student Name: " + studentName);
        System.out.println("Student Age: " + studentAge);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int id = sc.nextInt();
        String name = sc.next();
        int age = sc.nextInt();

        prog s = new prog(id, name, age);
        s.display();
    }
}
```

---

## **OUTPUT:**
<img width="547" height="424" alt="image" src="https://github.com/user-attachments/assets/adc7e45c-8c9a-4d37-8b49-75b8a3e0281a" />

---

## **RESULT:**

Thus, the Java program to implement variable scope and constructor was executed successfully.

---


