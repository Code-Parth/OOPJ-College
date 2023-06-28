# OOPJ-College Program-21

## Write a program to create a file name 123.txt, if it does not exist.  Append a new data to it if it already exist. write 150 integers  created randomly into the file using Text I/O. Integers are  separated by space. 

```JAVA
import java.io.*;
import java.util.Scanner;

public class FileAppendExample {
    public static void main(String[] args) {
        try (
                PrintWriter pw = new PrintWriter(new FileOutputStream(new File("123.txt"), true));) {
            for (int i = 0; i < 150; i++) {
                pw.print((int) (Math.random() * 150) + "\t ");
            }
        } catch (FileNotFoundException fnfe) {
            System.out.println("Cannot create the file.");
            fnfe.printStackTrace();
        }
    }
}

```

![image](https://github.com/Code-Parth/OOPJ-College/assets/84669955/24b6ef40-58e0-4aac-93bf-d5dc06178e38)

