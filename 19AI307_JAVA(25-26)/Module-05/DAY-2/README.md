
---

# **Ex.No:5(B) SERIALIZATION AND DESERIALIZATION**

## **QUESTION:**

Write a Java program to serialize and deserialize a collection of objects (for example, an `ArrayList<Student>`) using `ObjectOutputStream` and `ObjectInputStream`.

---

## **AIM:**

To write a Java program that performs **Serialization** (saving objects to a file) and **Deserialization** (retrieving objects from a file) using Java I/O streams.

---

## **ALGORITHM:**

1. Start the program.
2. Import the necessary packages: `java.io.*` and `java.util.*`.
3. Create the `Student` class and implement `Serializable`.
4. Create a list to store multiple `Student` objects.
5. Accept student details from the user and store them in the list.
6. Create a method to **serialize** the list of students into a file using `ObjectOutputStream`.
7. Create another method to **deserialize** the list from the file using `ObjectInputStream`.
8. Display the deserialized student objects.
9. End the program.

---

## **PROGRAM:**

```
/*
Program to implement Serialization and Deserialization using Java
Developed by: Arjun M
Register Number: 212222040012
*/
```

---

## **SOURCE CODE:**

```java
import java.io.*;
import java.util.*;

// Student class must implement Serializable
class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    // Serialize list of students
    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    // Deserialize list of students
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine(); // consume newline

        // Read student details from user
        for (int i = 0; i < n; i++) {
            int id = scanner.nextInt();
            scanner.nextLine(); // consume newline
            String name = scanner.nextLine();
            double marks = scanner.nextDouble();
            scanner.nextLine(); // consume newline

            students.add(new Student(id, name, marks));
        }

        String fileName = "students.dat";
        serializeStudents(students, fileName);

        List<Student> deserializedStudents = deserializeStudents(fileName);

        // Display deserialized data
        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}
```



## **OUTPUT:**

<img width="1165" height="249" alt="image" src="https://github.com/user-attachments/assets/ac0d5e8a-1b5f-4f56-9de0-5531896a0271" />


## **RESULT:**

Thus, the Java program to perform **Serialization and Deserialization** of a collection of objects was successfully executed.

---
