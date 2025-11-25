
---

# **Ex.No:3(E) INNER CLASS**

## **QUESTION:**

Write a Java program where a **private inner class** is declared inside an outer class and accessed through a public method of the outer class.

---

## **AIM:**

To study and implement **Inner Classes** in Java by creating a *private inner class* and accessing it using a method from the outer class.

---

## **ALGORITHM :**

1. Start the program.
2. Import the package `java.util`.
3. Create an outer class `Main`.
4. Declare a **private inner class** `Inner` with:

   * a private variable
   * a constructor
   * a display method
5. In the outer class, create a method `accessInner()` to create an inner-class object and call its display method.
6. In the main method, read input from user.
7. Call the method to access the inner class.
8. End the program.

---

## **PROGRAM:**

```
/*
Program to implement an Inner Class using Java
Developed by: 
RegisterNumber:  
*/
```

---

## **SOURCE CODE:**

```java
import java.util.Scanner;

public class Main {
    
    private class Inner {
        private int data;
        
        private Inner(int data) {
            this.data = data;
        }
        
        private void display() {
            System.out.println("Data set inside private inner class: " + data);
        }
    }
    
    public void accessInner(int value) {
        Inner inner = new Inner(value);
        inner.display();
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int value = sc.nextInt();
        
        Main outer = new Main();
        outer.accessInner(value);
        
        sc.close();
    }
}
```

---

## **OUTPUT:**

<img width="968" height="239" alt="image" src="https://github.com/user-attachments/assets/71f30840-00a8-4535-8399-6b44464322f4" />


---

## **RESULT:**

Thus, the Java program using a **private inner class accessed through an outer class method** was successfully executed.

---
