# OOPJ-College Program-02

## Write a program that solves the following equation and displays the value x and y:

### `Assume Cramer’s rule to solve equation ax+by=e, x=ed-bf/ad-bc, cx+dy=f, y=af-ec/ad-bc`

### 1) 3.4x+50.2y=44.5 
### 2) 2.1x+.55y=5.9

```java
public class LinearEquationSolver {
    public static void main(String[] args) {
        double a = 3.4, b = 50.2, c = 2.1, d = 0.55, e = 44.5, f = 5.9;

        // Calculate the determinant of the coefficient matrix
        double det = a * d - b * c;

        if (det == 0) {
            System.out.println("The equations have no solution");
        } else {
            // Calculate the values of x and y using Cramer's rule
            double x = (e * d - b * f) / det;
            double y = (a * f - e * c) / det;

            // Print out the values of x and y
            System.out.printf("x = %.2f, y = %.2f", x, y);
        }
    }
}
```

```
x = -6.08, y = 11.06
```
