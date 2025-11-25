

# **Ex.No:2(B) METHODS**

## **QUESTION:**

Write a Java program to create a method that calculates the cube of a given number.

---

## **AIM:**

To write a Java program that demonstrates the use of methods by creating a user-defined method to compute the cube of a number.

---

## **ALGORITHM :**

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class containing a method `square()` that accepts a number and returns its cube.
4. In the `main()` method, read a number from the user.
5. Create an object of the class.
6. Call the method and store the returned value.
7. Display the cube of the number.
8. End the program.

---

## **PROGRAM:**

```java
/*
Program to implement Methods using Java
Developed by: Arjun M
RegisterNumber: 212222040012
*/
```

---

## **SOURCE CODE:**

```java
import java.util.*;

class prog {
    public double square(double x)
    {
        return x * x * x;   // cube of the number
    }

    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        Double a = sc.nextDouble();

        prog obj = new prog();
        Double s = obj.square(a);

        System.out.println(s);
    }
}
```

---

## **OUTPUT:**

<img width="405" height="225" alt="image" src="https://github.com/user-attachments/assets/e40537d4-1208-4c42-b5d6-2775c0ad19b5" />


---

## **RESULT:**

Thus, the Java program using methods to find the cube of a number was executed successfully.

---

