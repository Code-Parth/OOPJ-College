# OOPJ-College Program-22

## Write a recursive method that returns the smallest integer in an  array. Write a test program that prompts the user to enter an integer  and display its product. 

```JAVA
import java.util.Scanner;

public class SmallestInteger {

    public static void main(String[] args) {
        // Create an array of integers
        int[] array = {5, 3, 9, 1, 7};

        // Find the smallest integer using the recursive method
        int smallest = findSmallest(array, array.length);

        // Display the smallest integer
        System.out.println("The smallest integer in the array is: " + smallest);

        // Prompt the user for an integer
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter an integer: ");
        int input = scanner.nextInt();

        // Calculate and display the product
        int product = calculateProduct(input);
        System.out.println("The product is: " + product);
    }

    // Recursive method to find the smallest integer in an array
    public static int findSmallest(int[] array, int length) {
        // Base case: If the length is 1, return the only element
        if (length == 1) {
            return array[0];
        }
        // Recursive case: Find the smallest integer in the subarray
        int subArraySmallest = findSmallest(array, length - 1);
        // Compare the smallest integer in the subarray with the current element
        if (array[length - 1] < subArraySmallest) {
            return array[length - 1];
        } else {
            return subArraySmallest;
        }
    }

    // Method to calculate the product of a number with itself
    public static int calculateProduct(int number) {
        return number * number;
    }
}

```

```

```
