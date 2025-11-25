---

# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM

## **QUESTION:**

Implement the Observer pattern where `MatchItServer` acts as the Subject and `User` acts as the Observer. Notify only those users whose preference matches the new signup's type.

---

## **AIM:**

To implement SOLID principles (focus on the Observer pattern / Single Responsibility & Open/Closed) by creating a notification system that alerts only matching users when a new person joins.

---

## **ALGORITHM :**

1. Start the program.
2. Import the necessary package `java.util`.
3. Create an `Observer` interface with `notify` and `getPreference` methods.
4. Implement `User` class as an Observer storing name and preference.
5. Create `MatchItServer` as Subject which maintains a list of observers and registers users.
6. When a new signup occurs, iterate observers and notify only those whose preference matches the new user's type.
7. In `main()`, read existing users and new signups from input and simulate notifications.
8. End the program.

---

## **PROGRAM:**

```java
/*
Program to implement a SOLID Principles in Java Program
Developed by: Arjun M
RegisterNumber: 212222040012
*/
```

---

## **SOURCE CODE:**

```java
import java.util.*;

interface Observer {
    void notify(String name, String type);
    String getPreference();
}

class User implements Observer {
    private String name;
    private String preference;

    public User(String name, String preference) {
        this.name = name;
        this.preference = preference;
    }

    public String getPreference() {
        return preference;
    }

    public void notify(String name, String type) {
        System.out.println(this.name + ": Omg! A new " + type + "? MatchIt, you know me too well! (It’s " + name + "!)");
    }
}

class MatchItServer {
    private List<Observer> users = new ArrayList<>();

    public void register(Observer o) {
        users.add(o);
    }

    public void newSignup(String name, String type) {
        System.out.println("New User Joined: " + name + " - Type: " + type);
        for (Observer o : users) {
            if (o.getPreference().equalsIgnoreCase(type)) {
                o.notify(name, type);
            }
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        MatchItServer server = new MatchItServer();

        int n = sc.nextInt(); sc.nextLine();
        for (int i = 0; i < n; i++) {
            String[] userInfo = sc.nextLine().split(" ");
            server.register(new User(userInfo[0], userInfo[1]));
        }

        int m = sc.nextInt(); sc.nextLine();
        for (int i = 0; i < m; i++) {
            String[] newUser = sc.nextLine().split(" ");
            server.newSignup(newUser[0], newUser[1]);
        }

        sc.close();
    }
}
```

---

## **OUTPUT:**
<img width="1209" height="482" alt="image" src="https://github.com/user-attachments/assets/79171997-23ec-4576-b4ce-373471d9bf05" />

## **RESULT:**

Thus, the Java program implementing the Observer pattern for MatchIt notifications was executed successfully.

---
