# OOPJ-College Program-15

## Write the bin2Dec (string binary String) method to convert a binary string into a decimal number. Implement the bin2Dec method to throw a NumberFormatException if the string is not a binary string.


```JAVA
public static int bin2Dec(String binaryString) throws NumberFormatException {
    if (!binaryString.matches("[01]+")) {
        throw new NumberFormatException("Not a binary string");
    }
    int decimal = 0;
    for (int i = 0; i < binaryString.length(); i++) {
        int bit = binaryString.charAt(i) - '0';
        decimal += bit * Math.pow(2, binaryString.length() - i - 1);
    }
    return decimal;
}

```

```

```
