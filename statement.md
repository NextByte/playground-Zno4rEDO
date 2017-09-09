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

// { autofold
public class Main {

public static void main(String[] args) {
// }

String message = "Hello World!";
System.out.println(message);

//{ autofold
}

}
//}
```

The author of this article is Alvin Alexander, the original article can be found on its blog [https://alvinalexander.com](https://alvinalexander.com/java/java-8-how-to-iterate-elements-map-hashmap).
