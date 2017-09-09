If you need to iterate over the elements in a Map in [Java 8](http://www.oracle.com/technetwork/java/javase/8-whats-new-2157071.html), this source code shows how to do it:

```java runnable
// { autofold
import java.util.HashMap;
import java.util.Map;

public class IterateOverJava8Map {
    
    public static void main(String[] args) {
        // }

Map<String, String> map = new HashMap<String, String>();
map.put("first_name", "Alvin");
map.put("last_name",  "Alexander");

// java 8
map.forEach((k,v)->System.out.println("key: " + k + ", value: " + v));

// { autofold

        // prior to java 8
        for (Map.Entry<String, String> entry : map.entrySet()) {
            System.out.println("key: " + entry.getKey() + ", value: " + entry.getValue());
        }

    }

}
// }
```
This approach uses an _anonymous function_ — also known as a _lambda_ — and it’s similar to the approach used to traverse a Map in Scala.

# How to iterate a Java 8 Map: A complete example
The following complete example shows how to iterate over all of the elements in a `Java Map` (or `HashMap`) using both a) the _Java 8_ style and b) the type of code you had to use prior to Java 8:

```java runnable
import java.util.HashMap;
import java.util.Map;

public class IterateOverJava8Map {
    
    public static void main(String[] args) {

        Map<String, String> map = new HashMap<String, String>();
        map.put("first_name", "Alvin");
        map.put("last_name",  "Alexander");
        
        // java 8
        map.forEach((k,v)->System.out.println("key: " + k + ", value: " + v));

        // prior to java 8
        for (Map.Entry<String, String> entry : map.entrySet()) {
            System.out.println("key: " + entry.getKey() + ", value: " + entry.getValue());
        }

    }

}
```

As a quick summary, if you needed to see how to iterate over the elements in a Map/HashMap in Java 8, I hope this is helpful.

The author of this article is Alvin Alexander, the original article can be found on its blog [https://alvinalexander.com](https://alvinalexander.com/java/java-8-how-to-iterate-elements-map-hashmap).
