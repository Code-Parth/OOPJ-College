# OOPJ-College Program-04

## Body Mass Index (BMI) is a measure of health on weight. It can be calculated by taking your weight in kilograms and dividing by the square of your height in meters. Write a program that prompts the user to enter a weight in pounds and height in inches and displays the BMI. Note:- 1 pound=.45359237 Kg and 1 inch=.0254 meters.

```java
import java.util.Scanner;

public class BMICalculator {
    public static void main(String[] args) {
        // Create a Scanner object to read input from the console
        Scanner scanner = new Scanner(System.in);

        // Prompt the user to enter weight in pounds
        System.out.print("Enter weight in pounds: ");

        // Read the weight in pounds from the user
        double weightInPounds = scanner.nextDouble();

        // Prompt the user to enter height in inches
        System.out.print("Enter height in inches: ");

        // Read the height in inches from the user
        double heightInInches = scanner.nextDouble();

        // Convert weight from pounds to kilograms
        double weightInKilograms = weightInPounds * 0.45359237;

        // Convert height from inches to meters
        double heightInMeters = heightInInches * 0.0254;

        // Calculate the BMI
        double bmi = weightInKilograms / Math.pow(heightInMeters, 2);

        // Display the result
        System.out.printf("Your BMI is %.2f", bmi);

        // Close the scanner
        scanner.close();
    }
}
```

```
Enter weight in pounds: 150
Enter height in inches: 65
Your BMI is 24.96
```
