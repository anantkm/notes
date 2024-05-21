
# Java Concurrent Collections How-Tos

## ConcurrentHashMap
```java
import java.util.concurrent.ConcurrentHashMap;

public class ConcurrentHashMapExample {
    public static void main(String[] args) {
        ConcurrentHashMap<String, Integer> map = new ConcurrentHashMap<>();
        
        // Add key-value pairs to ConcurrentHashMap
        map.put("Apple", 1);
        map.put("Banana", 2);

        // Access elements
        int count = map.get("Apple");

        // Remove elements
        map.remove("Banana");

        // Iterate through ConcurrentHashMap
        for (ConcurrentHashMap.Entry<String, Integer> entry : map.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }
    }
}
// Important Methods: put(), get(), remove(), containsKey(), containsValue(), keySet(), values(), entrySet(), size(), clear()
```

## ConcurrentSkipListMap
```java
import java.util.concurrent.ConcurrentSkipListMap;

public class ConcurrentSkipListMapExample {
    public static void main(String[] args) {
        ConcurrentSkipListMap<String, Integer> map = new ConcurrentSkipListMap<>();
        
        // Add key-value pairs to ConcurrentSkipListMap
        map.put("Apple", 1);
        map.put("Banana", 2);

        // Access elements
        int count = map.get("Apple");

        // Remove elements
        map.remove("Banana");

        // Iterate through ConcurrentSkipListMap
        for (ConcurrentSkipListMap.Entry<String, Integer> entry : map.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }
    }
}
// Important Methods: put(), get(), remove(), containsKey(), containsValue(), firstKey(), lastKey(), keySet(), values(), entrySet(), size(), clear()
```

## ConcurrentSkipListSet
```java
import java.util.concurrent.ConcurrentSkipListSet;

public class ConcurrentSkipListSetExample {
    public static void main(String[] args) {
        ConcurrentSkipListSet<String> set = new ConcurrentSkipListSet<>();
        
        // Add elements to ConcurrentSkipListSet
        set.add("Apple");
        set.add("Banana");

        // Check if an element exists
        boolean exists = set.contains("Apple");

        // Remove elements
        set.remove("Banana");

        // Iterate through ConcurrentSkipListSet
        for (String item : set) {
            System.out.println(item);
        }
    }
}
// Important Methods: add(), remove(), contains(), isEmpty(), size(), clear(), iterator(), first(), last(), higher(), lower()
```

## CopyOnWriteArrayList
```java
import java.util.concurrent.CopyOnWriteArrayList;

public class CopyOnWriteArrayListExample {
    public static void main(String[] args) {
        CopyOnWriteArrayList<String> list = new CopyOnWriteArrayList<>();
        
        // Add elements to CopyOnWriteArrayList
        list.add("Apple");
        list.add("Banana");

        // Access elements
        String fruit = list.get(0);

        // Remove elements
        list.remove("Banana");
        list.remove(0);

        // Iterate through CopyOnWriteArrayList
        for (String f : list) {
            System.out.println(f);
        }
    }
}
// Important Methods: add(), get(), remove(), size(), clear(), contains(), iterator()
```

## CopyOnWriteArraySet
```java
import java.util.concurrent.CopyOnWriteArraySet;

public class CopyOnWriteArraySetExample {
    public static void main(String[] args) {
        CopyOnWriteArraySet<String> set = new CopyOnWriteArraySet<>();
        
        // Add elements to CopyOnWriteArraySet
        set.add("Apple");
        set.add("Banana");

        // Check if an element exists
        boolean exists = set.contains("Apple");

        // Remove elements
        set.remove("Banana");

        // Iterate through CopyOnWriteArraySet
        for (String item : set) {
            System.out.println(item);
        }
    }
}
// Important Methods: add(), remove(), contains(), isEmpty(), size(), clear(), iterator()
```

## ConcurrentLinkedQueue
```java
import java.util.concurrent.ConcurrentLinkedQueue;

public class ConcurrentLinkedQueueExample {
    public static void main(String[] args) {
        ConcurrentLinkedQueue<String> queue = new ConcurrentLinkedQueue<>();
        
        // Add elements to ConcurrentLinkedQueue
        queue.add("Apple");
        queue.add("Banana");

        // Access and remove the head of the Queue
        String fruit = queue.poll(); // Removes and returns the head

        // Access the head without removing
        fruit = queue.peek(); // Returns the head

        // Iterate through ConcurrentLinkedQueue
        for (String item : queue) {
            System.out.println(item);
        }
    }
}
// Important Methods: add(), poll(), peek(), remove(), size(), clear(), iterator()
```

## ConcurrentLinkedDeque
```java
import java.util.concurrent.ConcurrentLinkedDeque;

public class ConcurrentLinkedDequeExample {
    public static void main(String[] args) {
        ConcurrentLinkedDeque<String> deque = new ConcurrentLinkedDeque<>();
        
        // Add elements to ConcurrentLinkedDeque
        deque.add("Apple");
        deque.add("Banana");

        // Access and remove elements from both ends
        String fruit = deque.pollFirst(); // Removes and returns the first element
        fruit = deque.pollLast(); // Removes and returns the last element

        // Access elements without removing
        fruit = deque.peekFirst(); // Returns the first element
        fruit = deque.peekLast(); // Returns the last element

        // Iterate through ConcurrentLinkedDeque
        for (String item : deque) {
            System.out.println(item);
        }
    }
}
// Important Methods: add(), pollFirst(), pollLast(), peekFirst(), peekLast(), remove(), size(), clear(), iterator()
```
