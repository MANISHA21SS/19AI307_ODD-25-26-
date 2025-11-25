# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:

<img width="1270" height="840" alt="Screenshot 2025-11-25 054801" src="https://github.com/user-attachments/assets/012bdf00-0130-4cac-aa4f-e70b9137c42d" />


## AIM:

To write a Java program using inheritance where a jewelry store calculates the final price for Regular and Premium customers based on gold rate per gram, purchase weight, discounts, and cashback (for Premium customers).

## ALGORITHM :

1.Start the program.

2.Create a Customer base class with:

Attributes: customerId, name, purchaseWeight, goldRatePerGram

Methods:

getDiscountRate() → returns 0

calculateFinalPrice() → returns price after discount

display() → prints details

3.Create RegularCustomer class extending Customer:

Override getDiscountRate() to return 2%

Override display() to show customer type and final price.

4.Create PremiumCustomer class extending Customer:

Override getDiscountRate() to return 5%

Add method to calculate 1% cashback of final price.

Override display() to print cashback also.

5.In main():

Accept gold rate from user.

Create objects for RegularCustomer and PremiumCustomer.

Display the bill details for each customer.

6.End program.





## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber: 212223220055 
*/

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
        System.out.println("Discount: " +(int) getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

// Regular Customer subclass
class RegularCustomer extends Customer {
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 2;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " +(int) getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

// Premium Customer subclass
class PremiumCustomer extends Customer {
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 5;
    }

    double calculateCashback() {
        return calculateFinalPrice() * 0.01;
    }

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
        Scanner sc = new Scanner(System.in);

        String type = sc.next();
        String customerId = sc.next();
        String name = sc.next();
        double purchaseWeight = sc.nextDouble();
        double goldRatePerGram = sc.nextDouble();

        Customer customer;
        if (type.equalsIgnoreCase("Regular")) {
            customer = new RegularCustomer(customerId, name, purchaseWeight, goldRatePerGram);
        } else if (type.equalsIgnoreCase("Premium")) {
            customer = new PremiumCustomer(customerId, name, purchaseWeight, goldRatePerGram);
        } else {
            customer = new Customer(customerId, name, purchaseWeight, goldRatePerGram);
        }

        customer.display();
    }
}

```

## OUTPUT:

<img width="1235" height="714" alt="Screenshot 2025-11-25 055258" src="https://github.com/user-attachments/assets/f867ef9e-96d3-404c-b5f0-27333a3c64ae" />


## RESULT:

Thus, the program is executed successfully to write a Java program using inheritance where a jewelry store calculates the final price for Regular and Premium customers based on gold rate per gram, purchase weight, discounts, and cashback.
