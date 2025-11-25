

# **Ex.No:2(A) CLASS AND OBJECT**

## **QUESTION:**

Create a class **Vehicle** with attributes: **number**, **type**, and **owner**.

---

## **AIM:**

To write a Java program that implements class and object concepts by creating a class `Vehicle` with attributes and printing details of two vehicle objects.

---

## **ALGORITHM :**

1. Start the program.
2. Import the package `java.util`.
3. Create a class `v` with attributes: number, type, and owner.
4. Create a parameterized constructor to initialize the values.
5. Create getter methods to return each attribute.
6. In the `main()` method, read details of two vehicles.
7. Create two `v` objects using the constructor.
8. Display the details of both vehicles.
9. End the program.

---

## **PROGRAM:**

```java
/*
Program to implement a Class and Objects using Java
Developed by: Arjun M
RegisterNumber: 212222040012
*/
```

---

## **SOURCE CODE:**

```java
import java.util.*;

class v {
    private String n;
    private String t;
    private String o;

    public v(String n, String t, String o)
    {
        this.n = n;
        this.t = t;
        this.o = o;
    }

    public String gn() {
        return n;
    }

    public String gt() {
        return t;
    }

    public String go() {
        return o;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String number, type, owner;

        number = sc.next();
        type = sc.next();
        owner = sc.next();
        v v1 = new v(number, type, owner);

        number = sc.next();
        type = sc.next();
        owner = sc.next();
        v v2 = new v(number, type, owner);

        System.out.println(v1.gn() + " | " + v1.gt() + " | " + v1.go());
        System.out.println(v2.gn() + " | " + v2.gt() + " | " + v2.go());

        sc.close();
    }
}
```

---

## **OUTPUT:**

<img width="823" height="289" alt="image" src="https://github.com/user-attachments/assets/0e603cc7-1f88-4da1-bd9c-ce93c87fc725" />


## **RESULT:**

Thus, the Java program demonstrating class and object concepts using a `Vehicle` class was executed successfully.

---

