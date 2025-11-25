

# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:

Write a Java program to implement Inheritance and Aggregation for a jewelry store gold rate calculation system.

## AIM:

To understand and implement Inheritance and Aggregation in Java using customer gold rate calculation.

## ALGORITHM :

1. Start the program.
2. Import the necessary packages.
3. Create the base class **Customer** with common attributes.
4. Create derived classes **RegularCustomer** and **PremiumCustomer**.
5. Apply discounts based on customer type.
6. For premium customers, calculate cashback.
7. Read user input and create the appropriate object.
8. Display the final output.
9. Stop the program.

---

## PROGRAM:

```
/*
Program to implement Inheritance and Aggregation using Java
Developed by: Arjun M
RegisterNumber: 212222040012
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;
import java.text.DecimalFormat;

class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    double getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class RegularCustomer extends Customer {
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    @Override
    double getDiscountRate() {
        return 2;
    }

    @Override
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: 2%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class PremiumCustomer extends Customer {
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    @Override
    double getDiscountRate() {
        return 5;
    }

    double calculateCashback() {
        return calculateFinalPrice() * 0.01;
    }

    @Override
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: 5%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(calculateCashback()));
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String customerType = scanner.next();
        String customerId = scanner.next();
        String name = scanner.next();
        double purchaseWeight = scanner.nextDouble();
        double goldRatePerGram = scanner.nextDouble();

        Customer customer;

        if (customerType.equals("Regular")) {
            customer = new RegularCustomer(customerId, name, purchaseWeight, goldRatePerGram);
        } else {
            customer = new PremiumCustomer(customerId, name, purchaseWeight, goldRatePerGram);
        }

        customer.display();
        scanner.close();
    }
}
```

---

## OUTPUT:

<img width="806" height="245" alt="image" src="https://github.com/user-attachments/assets/f4880525-981c-4dd7-a5d1-ae2491d3e492" />


---

## RESULT:

Thus the program to implement **Inheritance and Aggregation** in Java was successfully executed.

---
