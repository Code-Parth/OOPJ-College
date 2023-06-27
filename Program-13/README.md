# OOPJ-College Program-13

## Write a program for calculator to accept an expression as a string in which the operands and operator are separated by zero or more spaces.

## For ex: 3+4 and 3 + 4 are acceptable expressions


```JAVA
import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter an expression: ");
        String expression = input.nextLine();

        // Remove all spaces from the expression
        expression = expression.replaceAll("\\s", "");

        // Extract the operands and operator from the expression
        String[] operands = expression.split("[+\\-*/]");
        double num1 = Double.parseDouble(operands[0]);
        double num2 = Double.parseDouble(operands[1]);
        String operator = expression.replaceAll("[^+\\-*/]", "");

        // Calculate the result based on the operator
        double result = 0;
        switch (operator) {
            case "+":
                result = num1 + num2;
                break;
            case "-":
                result = num1 - num2;
                break;
            case "*":
                result = num1 * num2;
                break;
            case "/":
                result = num1 / num2;
                break;
            default:
                System.out.println("Invalid operator");
                return;
        }

        // Display the result
        System.out.println("Result: " + result);
    }
}

```

```
Enter an expression: 3+4
Result: 7.0
```
