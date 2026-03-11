# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
If an Integer object is set to null, and you attempt to call .toString() on it, what happens? How can you prevent your code from throwing an exception in such cases?

## AIM:
To understand what happens when calling a method (such as .toString()) on a null Integer object, and to learn how to prevent NullPointerException by using null checks or safe handling techniques in Java.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	If the input is 0, assign null to the Integer object num; otherwise, store the input value in num.
4.	Check whether num is null.
5.	If num is null, print "Null Integer"; otherwise, print the value of num.
6.	Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.*;

public class NullPointerExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int input = sc.nextInt(); 

        Integer num = (input == 0) ? null : input;

     
        System.out.println((num == null) ? "Null Integer" : num);

        sc.close();
    }
}
```






## OUTPUT:

<img width="500" height="302" alt="image" src="https://github.com/user-attachments/assets/170cecf7-6fca-4b97-8b9b-6ab8b96ca87f" />


## RESULT:

Thus the program to check if an Integer object is set to null, and you attempt to call .toString() on it is executed successfully.

