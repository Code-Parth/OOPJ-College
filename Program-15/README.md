# OOPJ-College Program-15

## Write the bin2Dec (string binary String) method to convert a binary string into a decimal number. Implement the bin2Dec method to throw a NumberFormatException if the string is not a binary string.


```JAVA
public class BinaryConverter {
    public static int bin2Dec(String binaryString) throws NumberFormatException {
        // Check if the string is empty or contains non-binary characters
        if (binaryString.isEmpty() || !binaryString.matches("[01]+")) {
            throw new NumberFormatException("Invalid binary string: " + binaryString);
        }

        int decimal = 0;
        int power = binaryString.length() - 1;

        // Convert binary string to decimal
        for (int i = 0; i < binaryString.length(); i++) {
            int digit = Character.getNumericValue(binaryString.charAt(i));
            decimal += digit * Math.pow(2, power);
            power--;
        }

        return decimal;
    }

    public static void main(String[] args) {
        String binaryString = "1101";

        try {
            int decimal = bin2Dec(binaryString);
            System.out.println("Binary: " + binaryString);
            System.out.println("Decimal: " + decimal);
        } catch (NumberFormatException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}

```

```
Binary: 1101
Decimal: 13
```
