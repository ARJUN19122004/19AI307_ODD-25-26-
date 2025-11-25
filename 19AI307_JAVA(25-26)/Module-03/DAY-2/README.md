
---

# **Ex.No:3(b) POLYMORPHISM**

## **QUESTION:**

Write a Java program that demonstrates runtime polymorphism using shapes.

## **AIM:**

To implement polymorphism in Java using method overriding with classes Shape, Circle, and Cylinder.

## **ALGORITHM :**

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a base class **Shape** with methods `draw()` and `calculateArea()`.
4. Create a subclass **Circle** that overrides both methods.
5. Create another subclass **Cylinder** that overrides both methods.
6. Read user input to select the shape and values (radius/height).
7. Create an object of the selected shape using polymorphism.
8. Call `draw()` and `calculateArea()` dynamically.
9. Display the results.
10. End the program.

---

## **PROGRAM:**

```
/*
Program to implement Polymorphism using Java
Developed by: Arjun M
RegisterNumber: 212222040012
*/
```

## **SOURCE CODE:**

```java
import java.util.Scanner;

class Shape {
    void draw() {
        System.out.println("Drawing a shape...");
    }

    double calculateArea() {
        return 0;
    }
}

class Circle extends Shape {
    double radius;

    Circle(double radius) {
        this.radius = radius;
    }

    @Override
    void draw() {
        System.out.println("Drawing a circle...");
    }

    @Override
    double calculateArea() {
        return Math.PI * radius * radius;
    }
}

class Cylinder extends Shape {
    double radius, height;

    Cylinder(double radius, double height) {
        this.radius = radius;
        this.height = height;
    }

    @Override
    void draw() {
        System.out.println("Drawing a cylinder...");
    }

    @Override
    double calculateArea() {
        // Total surface area = 2πr(h + r)
        return 2 * Math.PI * radius * (height + radius);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String shapeType = sc.next().toLowerCase();

        if (shapeType.equals("circle")) {
            double radius = sc.nextDouble();
            Shape s = new Circle(radius);
            s.draw();
            System.out.printf("Area: %.2f\n", s.calculateArea());
        } 
        else if (shapeType.equals("cylinder")) {
            double radius = sc.nextDouble();
            double height = sc.nextDouble();
            Shape s = new Cylinder(radius, height);
            s.draw();
            System.out.printf("Area: %.2f\n", s.calculateArea());
        } 
        else {
            System.out.println("Invalid shape type.");
        }

        sc.close();
    }
}
```

---

## **OUTPUT:**

<img width="634" height="330" alt="image" src="https://github.com/user-attachments/assets/658ee3ff-07f2-4aa7-be8a-9f65aea68183" />

---

## **RESULT:**

Thus, the Java program to demonstrate **Polymorphism using method overriding** was successfully executed.

---
