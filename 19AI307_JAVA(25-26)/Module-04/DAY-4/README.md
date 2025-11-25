
---

# Ex.No:4(D) DESIGN PATTERN — ABSTRACT FACTORY

## QUESTION:

## AIM:
To implement the Abstract Factory (simple factory) design pattern in Java to load different OS shells based on user input.

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create the interface and factory classes.
4. Get shell type from user.
5. Use factory to create correct shell.
6. Display output.

---

## PROGRAM:

/*
Program to implement an Abstract Factory Pattern using Java
Developed by: Arjun M
RegisterNumber: 212222040012
*/

---

## SOURCE CODE:

```java
import java.util.*;

interface Shell {
    void load();
}

class WindowsShell implements Shell {
    public void load() {
        System.out.println("Windows Shell loaded");
    }
}

class LinuxShell implements Shell {
    public void load() {
        System.out.println("Linux Shell loaded");
    }
}

class MacShell implements Shell {
    public void load() {
        System.out.println("Mac Shell loaded");
    }
}

class ShellFactory {
    public static Shell getShell(String os) {
        os = os.toLowerCase();
        switch (os) {
            case "windows":
                return new WindowsShell();
            case "linux":
                return new LinuxShell();
            case "mac":
                return new MacShell();
            default:
                return null;
        }
    }
}

public class ShellLoader {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String os = sc.nextLine().trim();
        String command = sc.nextLine().trim(); // second line

        if (command.equalsIgnoreCase("exit")) {
            System.out.println("Invalid OS: " + os);
        } else {
            Shell shell = ShellFactory.getShell(os);
            if (shell != null) {
                shell.load();
            } else {
                System.out.println("Invalid OS: " + os);
            }
        }

        sc.close();
    }
}
```

---

## OUTPUT:
<img width="592" height="300" alt="image" src="https://github.com/user-attachments/assets/d7b5367b-8739-437c-8418-01378755f075" />


## RESULT:

The Abstract Factory Pattern program was successfully implemented to load OS shells based on user input.

---
