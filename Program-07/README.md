# OOPJ-College Program-07

## Assume a vehicle plate number consists of three uppercase letters followed by four digits. Write a program to generate a plate number.


```JAVA
import java.util.Random;

public class PlateNumberGenerator {
    public static void main(String[] args) {
        // Create a Random object to generate random numbers
        Random rand = new Random();

        // Generate three random uppercase letters using ASCII codes
        char letter1 = (char) (rand.nextInt(26) + 'A');
        char letter2 = (char) (rand.nextInt(26) + 'A');
        char letter3 = (char) (rand.nextInt(26) + 'A');

        // Generate four random digits between 0 and 9
        int digit1 = rand.nextInt(10);
        int digit2 = rand.nextInt(10);
        int digit3 = rand.nextInt(10);
        int digit4 = rand.nextInt(10);

        // Concatenate the letters and digits to form the plate number
        String plateNumber = "" + letter1 + letter2 + letter3 + digit1 + digit2 + digit3 + digit4;

        // Display the plate number
        System.out.println("Generated plate number: " + plateNumber);
    }
}

```

```
Generated plate number: WZM4589

```
