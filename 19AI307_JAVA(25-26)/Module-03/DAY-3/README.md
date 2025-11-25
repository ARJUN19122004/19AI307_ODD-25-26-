
---

# **Ex.No:3(C) ABSTRACTION**

## **QUESTION:**

Write a Java program to implement abstraction using an abstract class **GameScore** with the method `finalScore()`.
Create subclasses **ArcadeGame** and **PuzzleGame** to compute scores differently.

---

## **AIM:**

To implement abstraction in Java using abstract classes and overridden abstract methods.

---

## **ALGORITHM :**

1. Start the program.
2. Import the package `java.util`.
3. Create an abstract class **GameScore** with abstract method `finalScore()`.
4. Create subclass **ArcadeGame** that calculates score as:
   `score = baseScore + (level × 100)`
5. Create subclass **PuzzleGame** that calculates score as:

   * If attempts ≤ 3 → `score = 1000 - (attempts × 100)`
   * Else → `score = 500`
6. Read user input:

   * If input = 1 → create ArcadeGame.
   * Else → create PuzzleGame.
7. Call `finalScore()` using abstraction.
8. Display the result.
9. End the program.

---

## **PROGRAM:**

```
/*
Program to implement Abstraction using Java
Developed by: Arjun M
RegisterNumber: 212222040012
*/
```

---

## **SOURCE CODE:**

```java
import java.util.*;

abstract class GameScore {
    abstract int finalScore();
}

class ArcadeGame extends GameScore {
    int base, level;
    ArcadeGame(int base, int level) {
        this.base = base;
        this.level = level;
    }
    int finalScore() {
        return base + (level * 100);
    }
}

class PuzzleGame extends GameScore {
    int attempts;
    PuzzleGame(int attempts) {
        this.attempts = attempts;
    }
    int finalScore() {
        if (attempts <= 3)
            return 1000 - (attempts * 100);
        else
            return 500;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();
        GameScore game;

        if (type == 1) {
            int base = sc.nextInt();
            int level = sc.nextInt();
            game = new ArcadeGame(base, level);
        } else {
            int attempts = sc.nextInt();
            game = new PuzzleGame(attempts);
        }

        System.out.println(game.finalScore());
    }
}
```

---

## **OUTPUT:**
<img width="332" height="203" alt="image" src="https://github.com/user-attachments/assets/485ffe38-aabd-4e62-94a5-73189dfafcbc" />


---

## **RESULT:**

Thus, the Java program to implement **Abstraction using abstract classes and overridden methods** was successfully executed.

---

