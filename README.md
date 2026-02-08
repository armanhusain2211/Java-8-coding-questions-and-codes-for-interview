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






