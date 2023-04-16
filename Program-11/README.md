# OOPJ-College Program-11

## Write a program that generate 6*6 two-dimensional matrix, filled with 0’s and 1’s , display the matrix, check every row and column have an odd number of 1’s.


```JAVA
import java.util.Random;

public class Matrix {
    public static void main(String[] args) {
        // Create a 6x6 matrix of 0's and 1's
        int[][] matrix = new int[6][6];
        Random rand = new Random();
        for (int i = 0; i < 6; i++) {
            for (int j = 0; j < 6; j++) {
                matrix[i][j] = rand.nextInt(2);
            }
        }

        // Display the matrix
        System.out.println("Matrix:");
        for (int i = 0; i < 6; i++) {
            for (int j = 0; j < 6; j++) {
                System.out.print(matrix[i][j] + " ");
            }
            System.out.println();
        }

        // Check that every row and column has an odd number of 1's
        boolean rowOdd = true;
        boolean colOdd = true;
        for (int i = 0; i < 6; i++) {
            int rowSum = 0;
            int colSum = 0;
            for (int j = 0; j < 6; j++) {
                rowSum += matrix[i][j];
                colSum += matrix[j][i];
            }
            if (rowSum % 2 == 0) {
                rowOdd = false;
            }
            if (colSum % 2 == 0) {
                colOdd = false;
            }
        }

        // Display the result
        if (rowOdd && colOdd) {
            System.out.println("Every row and column has an odd number of 1's.");
        } else {
            System.out.println("Not every row and column has an odd number of 1's.");
        }
    }
}

```

```
Matrix:
1 0 0 0 1 0 
1 1 1 1 1 0 
0 0 1 0 0 0 
1 0 1 1 1 0 
1 0 1 1 1 1 
0 0 1 0 1 1 
Every row and column has an odd number of 1's.

```
