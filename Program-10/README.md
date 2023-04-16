# OOPJ-College Program-10

## Write a test program that prompts the user to enter ten numbers, invoke a method to reverse the numbers, display the numbers.


```JAVA
import java.util.Scanner;

public class ReverseNumbers {
    public static void main(String[] args) {
        // Create a Scanner object to read input from the user
        Scanner input = new Scanner(System.in);

        // Read ten numbers from the user
        System.out.print("Enter ten numbers: ");
        int[] numbers = new int[10];
        for (int i = 0; i < 10; i++) {
            numbers[i] = input.nextInt();
        }

        // Reverse the order of the numbers
        reverse(numbers);

        // Display the reversed numbers
        System.out.print("The reversed numbers are: ");
        for (int i = 0; i < 10; i++) {
            System.out.print(numbers[i] + " ");
        }
    }

    // Reverse the order of an array of integers
    public static void reverse(int[] array) {
        int left = 0;
        int right = array.length - 1;
        while (left < right) {
            int temp = array[left];
            array[left] = array[right];
            array[right] = temp;
            left++;
            right--;
        }
    }
}

```

```
Enter ten numbers: 1 2 3 4 5 6 7 8 9 10
The reversed numbers are: 10 9 8 7 6 5 4 3 2 1

```
