# OOPJ-College Program-21

## Write a program to create a file name 123.txt, if it does not exist.  Append a new data to it if it already exist. write 150 integers  created randomly into the file using Text I/O. Integers are  separated by space. 

```JAVA
import java.io.BufferedWriter;
import java.io.FileWriter;
import java.io.IOException;
import java.util.Random;

public class FileAppendExample {
    public static void main(String[] args) {
        String fileName = "123.txt";

        try {
            FileWriter fileWriter = new FileWriter(fileName, true); // Append mode
            BufferedWriter bufferedWriter = new BufferedWriter(fileWriter);

            Random random = new Random();

            for (int i = 0; i < 150; i++) {
                int randomNumber = random.nextInt();
                bufferedWriter.write(String.valueOf(randomNumber));
                bufferedWriter.write(" ");
            }

            bufferedWriter.close();
            System.out.println("Data has been written to the file.");

        } catch (IOException e) {
            System.out.println("An error occurred: " + e.getMessage());
        }
    }
}

```

```

```
