# OOPJ-College Program-14

## Write a program that creates an Array List and adds a Loan object , a Date object , a string, and a Circle object to the list, and uses a loop to display all elements in the list by invoking the object's String() method.


```JAVA
import java.util.ArrayList;
import java.util.Date;

public class ArrayListExample {
    public static void main(String[] args) {
        // Create an ArrayList
        ArrayList<Object> list = new ArrayList<>();

        // Add objects to the list
        list.add(new Loan(1000.0, 5.0, 12));
        list.add(new Date());
        list.add("Hello, World!");
        list.add(new Circle(5.0));

        // Display all elements in the list
        for (Object obj : list) {
            System.out.println(obj.toString());
        }
    }
}

class Loan {
    private double amount;
    private double interestRate;
    private int term;

    public Loan(double amount, double interestRate, int term) {
        this.amount = amount;
        this.interestRate = interestRate;
        this.term = term;
    }

    public double getAmount() {
        return amount;
    }

    public double getInterestRate() {
        return interestRate;
    }

    public int getTerm() {
        return term;
    }

    public String toString() {
        return "Loan amount: " + amount + ", interest rate: " + interestRate + ", term: " + term;
    }
}

class Circle {
    private double radius;

    public Circle(double radius) {
        this.radius = radius;
    }

    public double getRadius() {
        return radius;
    }

    public double getArea() {
        return Math.PI * radius * radius;
    }

    public String toString() {
        return "Circle radius: " + radius + ", area: " + getArea();
    }
}

```

```
Loan amount: 1000.0,
interest rate: 5.0,
term: 12Tue Jun 27 14:17:21 GMT 2023
Hello, World!
Circle radius: 5.0,
area: 78.53981633974483
```
