# OOPJ-College Program-24

## Define MYPriorityQueue class that extends Priority Queue to  implement the Cloneable interface and implement the clone()  method to clone a priority queue. 

```JAVA
import java.util.PriorityQueue;

public class MYPriorityQueue<T> extends PriorityQueue<T> implements Cloneable {
  
  @Override
  public MYPriorityQueue<T> clone() {
    MYPriorityQueue<T> clonedQueue = new MYPriorityQueue<>();
    clonedQueue.addAll(this);
    return clonedQueue;
  }
  
  // Add other methods or overrides as needed
  
  public static void main(String[] args) {
    MYPriorityQueue<Integer> originalQueue = new MYPriorityQueue<>();
    originalQueue.add(5);
    originalQueue.add(2);
    originalQueue.add(8);
    
    // Clone the original priority queue
    MYPriorityQueue<Integer> clonedQueue = originalQueue.clone();
    
    // Test the cloned queue
    System.out.println("Original Queue: " + originalQueue);      // Output: Original Queue: [2, 5, 8]
    System.out.println("Cloned Queue: " + clonedQueue);          // Output: Cloned Queue: [2, 5, 8]
    
    // Modify the original queue
    originalQueue.add(10);
    
    // Test the modified original queue and cloned queue
    System.out.println("Original Queue (after modification): " + originalQueue);   // Output: Original Queue (after modification): [2, 5, 8, 10]
    System.out.println("Cloned Queue (should remain unchanged): " + clonedQueue);  // Output: Cloned Queue (should remain unchanged): [2, 5, 8]
  }
}

```

```

```
