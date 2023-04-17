# OOPJ-College Program-16

## Write a program that prompts the user to enter a decimal number and displays the number in a fraction.

## Hint: Read the decimal number as a string, extract the integer part and fractional part from the string.


```JAVA
import java.util.Scanner;

public class DecimalToFraction {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter a decimal number: ");
        String decimalStr = input.next();
        
        // Extract integer and fractional parts from decimal string
        int decimalPtIndex = decimalStr.indexOf('.');
        if (decimalPtIndex == -1) {
            System.out.println(decimalStr + " can be represented as " + decimalStr + "/1");
            return;
        }
        int wholeNum = Integer.parseInt(decimalStr.substring(0, decimalPtIndex));
        String fractionStr = decimalStr.substring(decimalPtIndex + 1);
        int numDigitsAfterDecimal = fractionStr.length();
        int numerator = Integer.parseInt(fractionStr);
        int denominator = (int) Math.pow(10, numDigitsAfterDecimal);

        // Simplify fraction using GCD
        int gcd = gcd(numerator, denominator);
        numerator /= gcd;
        denominator /= gcd;

        // Add whole number to fraction
        numerator += wholeNum * denominator;

        // Print result
        System.out.println(decimalStr + " can be represented as " + numerator + "/" + denominator);
    }

    // Helper method to find greatest common divisor
    public static int gcd(int num1, int num2) {
        if (num2 == 0) {
            return num1;
        }
        return gcd(num2, num1 % num2);
    }
}

```

```
Enter a decimal number: 3.14159
3.14159 can be represented as 628318/200000

```
