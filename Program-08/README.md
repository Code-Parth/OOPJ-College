# OOPJ-College Program-08

## Write a program that reads an integer and displays all its smallest factors in increasing order. For example if input number is 120, the output should be as follows:2,2,2,3,5

```JAVA
import java.util.Scanner;

public class SmallestFactors {
    public static void main(String[] args) {
        // Create a Scanner object to read input from the user
        Scanner input = new Scanner(System.in);

        // Read an integer from the user
        System.out.print("Enter an integer: ");
        int num = input.nextInt();

        // Find and display all the smallest factors of the number
        System.out.print("Smallest factors of " + num + ": ");
        for (int factor = 2; factor <= num; factor++) {
            while (num % factor == 0) {
                System.out.print(factor + " ");
                num /= factor;
            }
        }
    }
}

```

```
Enter an integer: 120
Smallest factors of 120: 2 2 2 3 5 

```
