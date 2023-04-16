# OOPJ-College Program-09

## Write a method with the following method header.Public static int gcd(int num1, int num2) Write a program that prompts the user to enter two integers and compute the gcd of two integers.

```JAVA
import java.util.Scanner;

public class GCD {
    public static void main(String[] args) {
        // Create a Scanner object to read input from the user
        Scanner input = new Scanner(System.in);

        // Read two integers from the user
        System.out.print("Enter two integers: ");
        int num1 = input.nextInt();
        int num2 = input.nextInt();

        // Compute the GCD of the two integers and display the result
        int gcd = gcd(num1, num2);
        System.out.println("The GCD of " + num1 + " and " + num2 + " is " + gcd);
    }

    // Compute the GCD of two integers using the Euclidean algorithm
    public static int gcd(int num1, int num2) {
        while (num2 != 0) {
            int temp = num2;
            num2 = num1 % num2;
            num1 = temp;
        }
        return num1;
    }
}

```

```
Enter two integers: 24 36
The GCD of 24 and 36 is 12

```
