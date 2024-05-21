
# Java Synchronized Collections How-Tos

## Synchronized List
```java
import java.util.Collections;
import java.util.List;
import java.util.ArrayList;

public class SynchronizedListExample {
    public static void main(String[] args) {
        List<String> list = Collections.synchronizedList(new ArrayList<>());
        
        // Add elements to Synchronized List
        synchronized(list) {
            list.add("Apple");
            list.add("Banana");
        }

        // Access elements
        synchronized(list) {
            String fruit = list.get(0);
        }

        // Remove elements
        synchronized(list) {
            list.remove("Banana");
            list.remove(0);
        }

        // Iterate through Synchronized List
        synchronized(list) {
            for (String f : list) {
                System.out.println(f);
            }
        }
    }
}
// Important Methods: add(), get(), remove(), size(), clear(), contains()
```

## Synchronized Set
```java
import java.util.Collections;
import java.util.Set;
import java.util.HashSet;

public class SynchronizedSetExample {
    public static void main(String[] args) {
        Set<String> set = Collections.synchronizedSet(new HashSet<>());
        
        // Add elements to Synchronized Set
        synchronized(set) {
            set.add("Apple");
            set.add("Banana");
        }

        // Check if an element exists
        synchronized(set) {
            boolean exists = set.contains("Apple");
        }

        // Remove elements
        synchronized(set) {
            set.remove("Banana");
        }

        // Iterate through Synchronized Set
        synchronized(set) {
            for (String item : set) {
                System.out.println(item);
            }
        }
    }
}
// Important Methods: add(), remove(), contains(), isEmpty(), size(), clear(), iterator()
```

## Synchronized Map
```java
import java.util.Collections;
import java.util.Map;
import java.util.HashMap;

public class SynchronizedMapExample {
    public static void main(String[] args) {
        Map<String, Integer> map = Collections.synchronizedMap(new HashMap<>());
        
        // Add key-value pairs to Synchronized Map
        synchronized(map) {
            map.put("Apple", 1);
            map.put("Banana", 2);
        }

        // Access elements
        synchronized(map) {
            int count = map.get("Apple");
        }

        // Remove elements
        synchronized(map) {
            map.remove("Banana");
        }

        // Iterate through Synchronized Map
        synchronized(map) {
            for (Map.Entry<String, Integer> entry : map.entrySet()) {
                System.out.println(entry.getKey() + ": " + entry.getValue());
            }
        }
    }
}
// Important Methods: put(), get(), remove(), containsKey(), containsValue(), keySet(), values(), entrySet(), size(), clear()
```

## Synchronized SortedMap
```java
import java.util.Collections;
import java.util.SortedMap;
import java.util.TreeMap;

public class SynchronizedSortedMapExample {
    public static void main(String[] args) {
        SortedMap<String, Integer> sortedMap = Collections.synchronizedSortedMap(new TreeMap<>());
        
        // Add key-value pairs to Synchronized SortedMap
        synchronized(sortedMap) {
            sortedMap.put("Apple", 1);
            sortedMap.put("Banana", 2);
        }

        // Access elements
        synchronized(sortedMap) {
            int count = sortedMap.get("Apple");
        }

        // Remove elements
        synchronized(sortedMap) {
            sortedMap.remove("Banana");
        }

        // Iterate through Synchronized SortedMap
        synchronized(sortedMap) {
            for (SortedMap.Entry<String, Integer> entry : sortedMap.entrySet()) {
                System.out.println(entry.getKey() + ": " + entry.getValue());
            }
        }
    }
}
// Important Methods: put(), get(), remove(), containsKey(), containsValue(), firstKey(), lastKey(), keySet(), values(), entrySet(), size(), clear()
```

## Synchronized SortedSet
```java
import java.util.Collections;
import java.util.SortedSet;
import java.util.TreeSet;

public class SynchronizedSortedSetExample {
    public static void main(String[] args) {
        SortedSet<String> sortedSet = Collections.synchronizedSortedSet(new TreeSet<>());
        
        // Add elements to Synchronized SortedSet
        synchronized(sortedSet) {
            sortedSet.add("Apple");
            sortedSet.add("Banana");
        }

        // Check if an element exists
        synchronized(sortedSet) {
            boolean exists = sortedSet.contains("Apple");
        }

        // Remove elements
        synchronized(sortedSet) {
            sortedSet.remove("Banana");
        }

        // Iterate through Synchronized SortedSet
        synchronized(sortedSet) {
            for (String item : sortedSet) {
                System.out.println(item);
            }
        }
    }
}
// Important Methods: add(), remove(), contains(), isEmpty(), size(), clear(), iterator(), first(), last(), higher(), lower()
```
