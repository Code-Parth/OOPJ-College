# OOPJ-College Program-05

## Write a program that prompts the user to enter three integers and display the integers in decreasing order.

```JAVA
import java.util.Scanner;

public class DecreasingOrder {
    public static void main(String[] args) {
        // Create a Scanner object to read input from the console
        Scanner scanner = new Scanner(System.in);

        // Prompt the user to enter three integers
        System.out.print("Enter three integers: ");

        // Read the three integers from the user
        int num1 = scanner.nextInt();
        int num2 = scanner.nextInt();
        int num3 = scanner.nextInt();

        // Determine the largest number
        int largest = num1;
        if (num2 > largest) {
            largest = num2;
        }
        if (num3 > largest) {
            largest = num3;
        }

        // Determine the smallest number
        int smallest = num1;
        if (num2 < smallest) {
            smallest = num2;
        }
        if (num3 < smallest) {
            smallest = num3;
        }

        // Determine the middle number
        int middle = num1 + num2 + num3 - largest - smallest;

        // Display the integers in decreasing order
        System.out.printf("%d %d %d", largest, middle, smallest);

        // Close the scanner
        scanner.close();
    }
}

```

```
Enter three integers: 10 5 15
15 10 5

```
