# OOPJ-College Program-23

## Write a generic method that returns the minimum elements in a  two dimensional array. 

```JAVA
public class MinimumElementInArray {
    public static void main(String[] args) {
        Integer list[][] = new Integer[10][10];
        int value = 0;
        for (int i = 0; i < list.length; i++) {
            for (int j = 0; j < list[i].length; j++) {
                list[i][j] = ++value;
            }
        }
        System.out.println("Minimum no is = " + min(list));
    }

    public static <E extends Comparable<E>> E min(E list[][]) {
        E min = list[0][0];
        for (E[] elements : list) {
            for (E element : elements) {
                if (element.compareTo(min) < 0) {
                    min = element;
                }
            }
        }
        return min;
    }
}

```

```
Minimum no is = 1

```
