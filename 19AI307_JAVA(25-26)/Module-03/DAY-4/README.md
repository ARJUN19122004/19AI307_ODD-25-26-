
---

# **Ex.No:3(D) INTERFACE**

## **QUESTION:**

Write a Java program to implement **Interface** concepts using a weather prediction system.
Create an interface **WeatherBot** with method `predict(int temperature)`.
Implement two bots:

* **SunBot** → Predicts *HOT* if temperature > 30, else *MODERATE*
* **RainBot** → Predicts *COLD* if temperature < 20, else *WARM*

Take temperature and bot type as user input.

---

## **AIM:**

To understand and implement interfaces in Java by creating multiple classes that implement the same interface and provide different behaviors.

---

## **ALGORITHM :**

1. Start the program.
2. Import the package `java.util`.
3. Create an interface **WeatherBot** with abstract method `predict()`.
4. Create class **SunBot** implementing WeatherBot.
5. Create class **RainBot** implementing WeatherBot.
6. Read user input for temperature and bot type.
7. Create the corresponding bot object using interface reference.
8. Call `predict()` and display output.
9. End the program.

---

## **PROGRAM:**

```
/*
Program to implement Interface using Java
Developed by: Arjun M
RegisterNumber: 212222040012
*/
```

---

## **SOURCE CODE:**

```java
import java.util.*;

interface WeatherBot {
    String predict(int temperature);
}

class SunBot implements WeatherBot {
    public String predict(int temperature) {
        return (temperature > 30) ? "HOT" : "MODERATE";
    }
}

class RainBot implements WeatherBot {
    public String predict(int temperature) {
        return (temperature < 20) ? "COLD" : "WARM";
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int temperature = sc.nextInt();
        int botType = sc.nextInt();

        WeatherBot bot = (botType == 1) ? new SunBot() : new RainBot();
        System.out.println(bot.predict(temperature));
    }
}
```

---

## **OUTPUT:**

<img width="354" height="174" alt="image" src="https://github.com/user-attachments/assets/2de7acf2-629a-4640-904c-e1d9252a632a" />

---

## **RESULT:**

Thus, the Java program using **Interface implementation** for weather prediction bots was successfully executed.

---


