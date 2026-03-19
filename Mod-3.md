
# Exp No - 3

## TITLE : Abstraction

### AIM :
To demonstrate abstraction and runtime polymorphism by calculating interest for different bank accounts.

### ALGORITHM :
STEP 1 : Start

STEP 2 : Create an abstract class BankAccount with abstract method calculateInterest()

STEP 2 : Create subclasses SavingsAccount and FixedDepositAccount

STEP 3 : Override calculateInterest() in both classes

STEP 4 : Read account type and input values

STEP 5 : Create appropriate object using parent reference

STEP 6 : Call calculateInterest()

STEP 7 : Display the interest

STEP 8 : End

### PROGRAM :
```
import java.util.*;

// Abstract class
abstract class BankAccount {
    public abstract double calculateInterest();
}

// SavingsAccount subclass
class SavingsAccount extends BankAccount {
    private double balance;

    public SavingsAccount(double balance) {
        this.balance = balance;
    }

    @Override
    public double calculateInterest() {
        double rate = 0.04; // 4% annual interest
        return balance * rate;
    }
}

// FixedDepositAccount subclass
class FixedDepositAccount extends BankAccount {
    private double amount;
    private int years;

    public FixedDepositAccount(double amount, int years) {
        this.amount = amount;
        this.years = years;
    }

    @Override
    public double calculateInterest() {
        double rate = 0.07; // 7% annual interest
        return amount * rate * years;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int accountType = sc.nextInt();

        BankAccount account;

        if (accountType == 1) {
            double balance = sc.nextDouble();
            account = new SavingsAccount(balance);
        } else {
            double amount = sc.nextDouble();
            int years = sc.nextInt();
            account = new FixedDepositAccount(amount, years);
        }

        double interest = account.calculateInterest();
        System.out.printf("%.2f\n", interest);
    }
}

```

### OUTPUT :

<img width="360" height="364" alt="image" src="https://github.com/user-attachments/assets/62d6826f-6b10-46db-8da2-a2aea3d62a61" />

### RESULT :

Thus to demonstrate abstraction and runtime polymorphism by calculating interest for different bank accounts was successfully created.
