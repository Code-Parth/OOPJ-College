# OOPJ-College Program-12

## Write a program that creates a Random object with seed 1000 and displays the first 100 random integers between 1 and 49 using the NextInt (49) method.


```JAVA
import java.util.Random;

public class RandomIntegers {
    public static void main(String[] args) {
        Random rand = new Random(1000);

        for (int i = 1; i <= 100; i++) {
            int num = rand.nextInt(49) + 1;
            System.out.print(num + " ");

            if (i % 10 == 0) {
                System.out.println();
            }
        }
    }
}

```

```
41 2 18 1 47 47 5 34 10 41 
26 14 18 30 31 32 43 36 49 41 
12 14 11 1 39 10 1 11 36 11 
15 27 35 36 32 44 48 36 3 34 
17 49 46 44 6 30 2 36 1 26 
29 43 26 3 34 31 19 28 5 29 
32 36 10 14 34 13 19 37 40 8 18 32 22 27 48 40 12 41 12 27 
49 27 28 33 20 31 27 5 8 41 
10 42 9 38 4 35 11 37 5 22 
```
