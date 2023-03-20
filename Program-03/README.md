# OOPJ-College Program-03

## Write a program that reads a number in meters, converts it to feet, and displays the result.

```java
import java.util.Scanner;

public class LengthConverter {
    public static void main(String[] args) {
        // Create a Scanner object to read input from the console
        Scanner scanner = new Scanner(System.in);

        // Prompt the user to enter a length in meters
        System.out.print("Enter a length in meters: ");

        // Read the length in meters from the user
        double meters = scanner.nextDouble();

        // Convert the length from meters to feet
        double feet = meters * 3.28084;

        // Display the result
        System.out.printf("%.2f meters is equal to %.2f feet", meters, feet);

        // Close the scanner
        scanner.close();
    }
}
```

```
Enter a length in meters: 10
10.00 meters is equal to 32.81 feet
```
