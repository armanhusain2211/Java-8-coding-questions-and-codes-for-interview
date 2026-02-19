# Java-8-coding-questions-and-codes-for-interview
Interview Preparation


**Filter even numbers**

package p1;

import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;

public class Test {
    public static void main(String[] args) {

       List<Integer> list = Arrays.asList(2,4,9,7,6,1,8,10);
       List<Integer> evenNumbers =
    		   list.stream()
    		       .filter(i -> i % 2 == 0)
    		       .collect(Collectors.toList());
       System.out.println(evenNumbers);
        
    }
}

o/p
(2, 4, 6, 8, 10)

**Convert strings to uppercase**
package p1;

import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;

public class Test {
    public static void main(String[] args) {

       List<String> list = Arrays.asList("Arman", "Java", "DevOps");
       List<String> names =
    		   list.stream()
    		       .map(s -> s.toUpperCase())
    		       .collect(Collectors.toList());
       System.out.println(names);
        
    }
}

o/p
(ARMAN, JAVA, DEVOPS)

**Find frequency**

//Approach(HashMap)
List<Integer> list = Arrays.asList(1, 2, 3, 2, 1, 2);

Map<Integer, Integer> frequencyMap = new HashMap<>();

for (Integer num : list) {
    frequencyMap.put(num, frequencyMap.getOrDefault(num, 0) + 1);
}

System.out.println(frequencyMap);


//Approach(Java 8 Stream)

Map<Integer, Long> frequency = list.stream()
        .collect(Collectors.groupingBy(e -> e, Collectors.counting()));

System.out.println(frequency);


**Reverse a List**
//Approach(Two-pointer)

List<Integer> list = new ArrayList<>(Arrays.asList(1, 2, 3, 4, 5));

for (int i = 0; i < list.size() / 2; i++) {

    int temp = list.get(i);
    list.set(i, list.get(list.size() - 1 - i));
    list.set(list.size() - 1 - i, temp);
}

System.out.println(list);


//Approach(Collections.reverse)

import java.util.*;

public class ReverseExample {
    public static void main(String[] args) {

        List<Integer> list = new ArrayList<>(Arrays.asList(1, 2, 3, 4, 5));

        Collections.reverse(list);

        System.out.println(list);
    }
}



