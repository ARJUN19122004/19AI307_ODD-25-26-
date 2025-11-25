
---

# Ex.No:4(D) DESIGN PATTERN — BEHAVIOUR PATTERN (MVC)

## QUESTION:

Write a Java MVC program to track a Bank Account balance.
The Controller can deposit and withdraw, and the View should show the updated balance.

---

## AIM:

To implement the **MVC (Model–View–Controller)** Behavioural Design Pattern in Java for managing bank account operations.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create the **Model** class `BankAccount`.
4. Create the **View** class `AccountView` to display outputs.
5. Create the **Controller** class `AccountController` to control deposit and withdrawal actions.
6. Accept user input for initial balance and operations.
7. Call the controller methods to update the model and view.
8. Stop the program.

---

## PROGRAM:

/*
Program to implement a Behaviour Pattern (MVC) using Java
Developed by: Arjun M
RegisterNumber: 212222040012
*/

---

## SOURCE CODE:

```java
import java.util.*;

public class BankMVCSkeleton {

    // Model
    static class BankAccount {
        private double balance;

        public BankAccount(double initialBalance) {
            this.balance = initialBalance;
        }

        public void deposit(double amount) {
            balance += amount;
        }

        public boolean withdraw(double amount) {
            if (amount <= balance) {
                balance -= amount;
                return true;
            } else {
                return false;
            }
        }

        public double getBalance() {
            return balance;
        }
    }

    // View
    static class AccountView {
        public void showBalance(double balance) {
            System.out.printf("Current Balance: ₹%.2f%n", balance);
        }

        public void showError(String message) {
            System.out.println(message);
        }
    }

    // Controller
    static class AccountController {
        private BankAccount model;
        private AccountView view;

        public AccountController(BankAccount model, AccountView view) {
            this.model = model;
            this.view = view;
        }

        public void deposit(double amount) {
            model.deposit(amount);
            view.showBalance(model.getBalance());
        }

        public void withdraw(double amount) {
            if (model.withdraw(amount)) {
                view.showBalance(model.getBalance());
            } else {
                view.showError("Withdrawal failed: insufficient balance.");
            }
        }
    }

    // Main method
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        double initialBalance = sc.nextDouble();
        BankAccount model = new BankAccount(initialBalance);
        AccountView view = new AccountView();
        AccountController controller = new AccountController(model, view);

        int operations = sc.nextInt();
        for (int i = 0; i < operations; i++) {
            String op = sc.next();
            double amount = sc.nextDouble();
            if (op.equalsIgnoreCase("deposit")) {
                controller.deposit(amount);
            } else if (op.equalsIgnoreCase("withdraw")) {
                controller.withdraw(amount);
            }
        }

        sc.close();
    }
}
```

---

## OUTPUT:

<img width="1062" height="241" alt="image" src="https://github.com/user-attachments/assets/5618d54e-425e-40b1-9392-081cf2f46d41" />


---

## RESULT:

Thus, the program to implement the **Behaviour Pattern (MVC)** for Bank Account balance tracking was successfully executed.

---
