
---

# **Ex.No:2(C) ACCESS SPECIFIERS**

## **QUESTION:**

Write a Java program to create a class called **Rectangle** with private instance variables `length` and `width`. Provide public getter and setter methods to access and modify these variables.

---

## **AIM:**

To understand and implement access specifiers in Java by using private variables and public getter/setter methods.

---

## **ALGORITHM :**

1. Start the program.
2. Import the package `java.util`.
3. Create a class `Rectangle` with private variables `length` and `width`.
4. Provide public getter and setter methods to read and modify values.
5. In the `main()` method, create an object of `Rectangle`.
6. Read input values and set them using setter methods.
7. Print the values using getter methods.
8. End the program.

---

## **PROGRAM:**

```java
/*
Program to implement Access Specifiers using Java
Developed by: Arjun M
RegisterNumber: 212222040012
*/
```

---

## **SOURCE CODE:**

```java
import java.util.Scanner;

class Rectangle {
    private double length;
    private double width;

    public double getLength() {
        return length;
    }

    public void setLength(double length) {
        this.length = length;
    }

    public double getWidth() {
        return width;
    }

    public void setWidth(double width) {
        this.width = width;
    }
}

class prog {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        Rectangle rect = new Rectangle();
        rect.setLength(scanner.nextDouble());
        rect.setWidth(scanner.nextDouble());

        System.out.println("Length: " + rect.getLength());
        System.out.println("Width: " + rect.getWidth());

        scanner.close();
    }
}
```

---

## **OUTPUT:**
![Uploading image.png…]()



---

## **RESULT:**

Thus, the Java program using access specifiers with getter and setter methods was executed successfully.

---



