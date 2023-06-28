# OOPJ-College Program-22

## Write a recursive method that returns the smallest integer in an  array. Write a test program that prompts the user to enter an integer  and display its product. 

```JAVA
import java.util.Scanner;

public class SmallestInteger {
    public static int findMinimum(int A[], int n) {
        // if size = 0 means whole array has been traversed
        if (n == 1)
            return A[0];
        return Math.min(A[n - 1], findMinimum(A, n - 1));
    }

    // Driver code
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        System.out.println("How many elements you want in array?");
        int n = sc.nextInt();
        int A[] = new int[n];
        for (int i = 0; i < n; i++) {
            A[i] = sc.nextInt();
        }
        // Function calling
        System.out.println("Smallest element in the array is: " + findMinimum(A, n));
    }
}

```

```

```
