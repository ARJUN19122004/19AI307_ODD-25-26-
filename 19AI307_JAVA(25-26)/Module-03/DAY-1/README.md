---

# Ex.No:3(A) INHERITANCE AND AGGREGATION

## **QUESTION:**

A jewelry store tracks gold rates for different types of customers. The base class is `Customer` with attributes like `customerId`, `name`, and `purchaseWeight` (in grams). There are two types of customers: `RegularCustomer` and `PremiumCustomer`. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay and (for PremiumCustomer) the cashback amount.

---

## **AIM:**

To implement inheritance and aggregation by creating a base `Customer` class and derived classes `RegularCustomer` and `PremiumCustomer` that compute discounts, final price, and cashback.

---

## **ALGORITHM :**

1. Start the program.
2. Import the necessary package `java.util` and `java.text` for formatting.
3. Create a base class `Customer` with attributes: `customerId`, `name`, `purchaseWeight`, and `goldRatePerGram`.
4. Provide methods to compute discount rate (overridden by subclasses) and final price.
5. Create subclass `RegularCustomer` that returns 2% discount.
6. Create subclass `PremiumCustomer` that returns 5% discount and computes cashback as 1% of final price.
7. In `main()`, read customer type and details from input, instantiate the appropriate subclass, and call its `display()` method.
8. End the program.

---

## **PROGRAM:**

```java
/*
Program to implement Inheritance and Aggregation using Java
Developed by: Arjun M
RegisterNumber: 212222040012
*/
```

---

## **SOURCE CODE:**

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
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
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
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
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

## **OUTPUT:**
<img width="853" height="254" alt="image" src="https://github.com/user-attachments/assets/5685ce00-e613-4c5b-94b2-fe4625468866" />


## **RESULT:**

Thus, the Java program demonstrating inheritance and aggregation for customer gold-rate calculations was executed successfully.

---
