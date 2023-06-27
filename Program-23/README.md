# OOPJ-College Program-23

## Write a generic method that returns the minimum elements in a  two dimensional array. 

```JAVA
import java.util.Arrays;

public class MinimumElementInArray {

    public static <T extends Comparable<T>> T findMinimum(T[][] array) {
        if (array == null || array.length == 0 || array[0].length == 0) {
            throw new IllegalArgumentException("Invalid array");
        }

        T min = array[0][0];
        for (T[] row : array) {
            for (T element : row) {
                if (element.compareTo(min) < 0) {
                    min = element;
                }
            }
        }

        return min;
    }

    public static void main(String[] args) {
        Integer[][] intArray = {
                {3, 5, 1},
                {7, 2, 9},
                {4, 6, 8}
        };
        System.out.println("Minimum element in intArray: " + findMinimum(intArray));

        Double[][] doubleArray = {
                {3.5, 2.1, 4.7},
                {1.2, 5.3, 0.8},
                {6.9, 3.0, 2.7}
        };
        System.out.println("Minimum element in doubleArray: " + findMinimum(doubleArray));

        String[][] stringArray = {
                {"apple", "banana", "orange"},
                {"pear", "grape", "kiwi"},
                {"cherry", "strawberry", "pineapple"}
        };
        System.out.println("Minimum element in stringArray: " + findMinimum(stringArray));
    }
}

```

```

```
