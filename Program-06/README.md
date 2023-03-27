# OOPJ-College Program-06

## Write a program that prompts the user to enter a letter and check whether a letter is a vowel or constant.


```JAVA
import java.util.Scanner;

public class VowelOrConsonant {
    public static void main(String[] args) {
        // Create a Scanner object to read input from the console
        Scanner scanner = new Scanner(System.in);

        // Prompt the user to enter a letter
        System.out.print("Enter a letter: ");

        // Read a single character from the user
        char letter = scanner.nextLine().charAt(0);

        // Check if the letter is a vowel or a consonant
        if (letter == 'a' || letter == 'e' || letter == 'i' || letter == 'o' || letter == 'u'
                || letter == 'A' || letter == 'E' || letter == 'I' || letter == 'O' || letter == 'U') {
            System.out.printf("%c is a vowel", letter);
        } else if ((letter >= 'a' && letter <= 'z') || (letter >= 'A' && letter <= 'Z')) {
            System.out.printf("%c is a consonant", letter);
        } else {
            System.out.println("Invalid input: Please enter a letter");
        }

        // Close the scanner
        scanner.close();
    }
}

```

```
Enter a letter: a
a is a vowel

```
