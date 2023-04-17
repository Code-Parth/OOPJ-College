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

```
