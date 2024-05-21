
# Java Data Structures How-Tos

## ArrayList
```java
import java.util.ArrayList;

public class ArrayListExample {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        
        // Add elements to ArrayList
        list.add("Apple");
        list.add("Banana");

        // Access elements
        String fruit = list.get(0);

        // Remove elements
        list.remove("Banana");
        list.remove(0);

        // Iterate through ArrayList
        for (String f : list) {
            System.out.println(f);
        }
    }
}
// Important Methods: add(), get(), remove(), size(), clear(), contains()
```

## LinkedList
```java
import java.util.LinkedList;

public class LinkedListExample {
    public static void main(String[] args) {
        LinkedList<String> list = new LinkedList<>();
        
        // Add elements to LinkedList
        list.add("Apple");
        list.add("Banana");

        // Access elements
        String fruit = list.get(0);

        // Remove elements
        list.remove("Banana");
        list.remove(0);

        // Iterate through LinkedList
        for (String f : list) {
            System.out.println(f);
        }
    }
}
// Important Methods: add(), get(), remove(), size(), clear(), contains(), addFirst(), addLast(), removeFirst(), removeLast()
```

## Queue
```java
import java.util.Queue;
import java.util.LinkedList;

public class QueueExample {
    public static void main(String[] args) {
        Queue<String> queue = new LinkedList<>();
        
        // Add elements to Queue
        queue.add("Apple");
        queue.add("Banana");

        // Access and remove the head of the Queue
        String fruit = queue.poll(); // Removes and returns the head

        // Access the head without removing
        fruit = queue.peek(); // Returns the head

        // Iterate through Queue
        for (String item : queue) {
            System.out.println(item);
        }
    }
}
// Important Methods: add(), poll(), peek(), remove(), offer()
```

## Stack
```java
import java.util.ArrayDeque;
import java.util.Deque;

public class StackExample {
    public static void main(String[] args) {
        Deque<String> stack = new ArrayDeque<>();
        
        // Add elements to Stack
        stack.push("one");
        stack.push("two");

        // Access and remove the top of the Stack
        System.out.println(stack.pop()); // two
        System.out.println(stack.pop()); // one
    }
}
// Important Methods: push(), pop(), peek(), isEmpty(), size()
```

## HashMap
```java
import java.util.HashMap;

public class HashMapExample {
    public static void main(String[] args) {
        HashMap<String, Integer> map = new HashMap<>();
        
        // Add key-value pairs to HashMap
        map.put("Apple", 1);
        map.put("Banana", 2);

        // Access elements
        int count = map.get("Apple");

        // Remove elements
        map.remove("Banana");

        // Iterate through HashMap
        for (HashMap.Entry<String, Integer> entry : map.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }
    }
}
// Important Methods: put(), get(), remove(), containsKey(), containsValue(), keySet(), values(), entrySet(), size(), clear()
```

## HashSet
```java
import java.util.HashSet;

public class HashSetExample {
    public static void main(String[] args) {
        HashSet<String> set = new HashSet<>();
        
        // Add elements to HashSet
        set.add("Apple");
        set.add("Banana");

        // Check if an element exists
        boolean exists = set.contains("Apple");

        // Remove elements
        set.remove("Banana");

        // Iterate through HashSet
        for (String item : set) {
            System.out.println(item);
        }
    }
}
// Important Methods: add(), remove(), contains(), isEmpty(), size(), clear(), iterator()
```

## MinHeap (PriorityQueue)
```java
import java.util.PriorityQueue;

public class MinHeapExample {
    public static void main(String[] args) {
        PriorityQueue<Integer> minHeap = new PriorityQueue<>();
        
        // Add elements to MinHeap
        minHeap.add(10);
        minHeap.add(5);

        // Access and remove the root of the MinHeap
        int min = minHeap.poll(); // Removes and returns the root

        // Access the root without removing
        min = minHeap.peek(); // Returns the root

        // Iterate through MinHeap
        for (int item : minHeap) {
            System.out.println(item);
        }
    }
}
// Important Methods: add(), poll(), peek(), remove(), size(), clear(), iterator()
```

## MaxHeap (PriorityQueue)
```java
import java.util.PriorityQueue;
import java.util.Collections;

public class MaxHeapExample {
    public static void main(String[] args) {
        PriorityQueue<Integer> maxHeap = new PriorityQueue<>(Collections.reverseOrder());
        
        // Add elements to MaxHeap
        maxHeap.add(10);
        maxHeap.add(5);

        // Access and remove the root of the MaxHeap
        int max = maxHeap.poll(); // Removes and returns the root

        // Access the root without removing
        max = maxHeap.peek(); // Returns the root

        // Iterate through MaxHeap
        for (int item : maxHeap) {
            System.out.println(item);
        }
    }
}
// Important Methods: add(), poll(), peek(), remove(), size(), clear(), iterator()
```

## PriorityQueue
```java
import java.util.PriorityQueue;

public class PriorityQueueExample {
    public static void main(String[] args) {
        PriorityQueue<String> queue = new PriorityQueue<>();
        
        // Add elements to PriorityQueue
        queue.add("Apple");
        queue.add("Banana");

        // Access and remove the head of the PriorityQueue
        String fruit = queue.poll(); // Removes and returns the head

        // Access the head without removing
        fruit = queue.peek(); // Returns the head

        // Iterate through PriorityQueue
        for (String item : queue) {
            System.out.println(item);
        }
    }
}
// Important Methods: add(), poll(), peek(), remove(), size(), clear(), iterator()
```

## TreeMap
```java
import java.util.TreeMap;

public class TreeMapExample {
    public static void main(String[] args) {
        TreeMap<String, Integer> map = new TreeMap<>();
        
        // Add key-value pairs to TreeMap
        map.put("Apple", 1);
        map.put("Banana", 2);

        // Access elements
        int count = map.get("Apple");

        // Remove elements
        map.remove("Banana");

        // Iterate through TreeMap
        for (TreeMap.Entry<String, Integer> entry : map.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }
    }
}
// Important Methods: put(), get(), remove(), containsKey(), containsValue(), firstKey(), lastKey(), keySet(), values(), entrySet(), size(), clear()
```

## TreeSet
```java
import java.util.TreeSet;

public class TreeSetExample {
    public static void main(String[] args) {
        TreeSet<String> set = new TreeSet<>();
        
        // Add elements to TreeSet
        set.add("Apple");
        set.add("Banana");

        // Check if an element exists
        boolean exists = set.contains("Apple");

        // Remove elements
        set.remove("Banana");

        // Iterate through TreeSet
        for (String item : set) {
            System.out.println(item);
        }
    }
}
// Important Methods: add(), remove(), contains(), isEmpty(), size(), clear(), iterator(), first(), last(), higher(), lower()
```
