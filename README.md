# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:

A shop keeper would like to welcome their customers with their name.

Write a java program to get name from the user (String) and print it.

Input Format:

A single line string input.

Output Format:

Hello, [name]

For example:

Input	: Ajeesh 
Result : Hello, Ajeesh


## AIM:

Write a java program to get name from the user (String) and print it.


## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Create a Scanner object to read input from the user.
4.Read a string input (the user's name).
5.Store the input in the variable name.
6.Display the message: "Hello, " + name
```



## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: Madhuvathani v
RegisterNumber:  212223040107
*/
```

```
import java.util.*;
public class prog{
    public static void main(String[] args){
        Scanner sc= new Scanner(System.in);
        String name = sc.next();
        
        System.out.print("Hello, "+name);
    }
}
```



## OUTPUT:

<img width="669" height="242" alt="Screenshot 2025-11-19 104928" src="https://github.com/user-attachments/assets/fec616b3-c127-4715-a786-c3fc853b67b2" />


## RESULT:

Thus, the java program to get name from the user (String) and print it is executed successfully.


# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
A train company charges tickets based on age and travel class:

Children (<12): ₹5 per km (any class)

Adults (12–60):

Sleeper: ₹10/km

AC: ₹15/km

Seniors (>60): ₹7/km (any class)

Task: Accept age, distance and travel class (1 for Sleeper, 2 for AC)(follow the same order to get the inputs). Calculate fare.

For example:

Input	
5
100
Result
500



## AIM:

To write a program that accepts the age, distance, and travel class (1 for Sleeper, 2 for AC) and calculates the train fare based on age-wise and class-wise fare rules.

## ALGORITHM :
```
1.Start and read the inputs: age, distance, and travel class.
2.Determine the rate per km based on age and class conditions.
3.If age < 12, set rate = 5;
   else if age 12–60, set rate = 10 for Sleeper or 15 for AC;
   else if age > 60, set rate = 7.
4.Calculate the fare using: fare = distance × rate.
5.Display the total fare and Stop.
```




## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: Madhuvathani v
RegisterNumber:  212223040107
*/
```

```
import java.util.Scanner;

public class TrainFare {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int age = sc.nextInt();
        int distance = sc.nextInt();

        int farePerKm=0;;

        if (age < 12) {
            farePerKm = 5;
        } else if (age > 60) {
            farePerKm = 7;
        } else { 
            int travelClass = sc.nextInt();
            if (travelClass == 1) {
                farePerKm = 10;
            } else if (travelClass == 2) {
                farePerKm = 15;
            } else {
                System.out.println("Invalid class");
                return;
            }
        }

        int totalFare = farePerKm * distance;
        System.out.println(totalFare);
    }
}
```


## OUTPUT:

<img width="652" height="356" alt="image" src="https://github.com/user-attachments/assets/492431f7-c261-4417-aecd-114541a862fd" />


## RESULT:

Thus, a java program to calculates the train fare based on age-wise and class-wise fare rules is executed successfully.

# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Sum of Prime Numbers up to N

For example:
Input	
10
Result
Sum of primes: 17



## AIM:
To write a program to Sum of Prime Numbers up to N


## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Initialize sum = 0 to store the total of all prime numbers.
4.If n ≤ 1, return false.
5.If any divisor is found, return false; otherwise, return true.
6.If isPrime(i) is true, add i to sum.
7.After the loop ends, print the sum of all prime numbers up to n.
```




## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.Scanner;
public class SumOfPrimes {
    public static boolean isPrime(int n) {
        if (n <= 1) return false;
        for (int i = 2; i <= Math.sqrt(n); i++) {
            if (n % i == 0) return false;
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int sum = 0;
        for (int i = 2; i <= n; i++) {
            if (isPrime(i)) {
                sum += i;
            }
        }
        System.out.println("Sum of primes: " + sum);
        sc.close();
    }
}
```

## OUTPUT:

<img width="665" height="321" alt="image" src="https://github.com/user-attachments/assets/d3771899-1833-4b8a-a2d8-84d3159f7492" />


## RESULT:

 Thus, the program to print Sum of Prime Numbers up to N is executed successfully.


# Ex.No:1(D) ARRAYS

## QUESTION:

Write a Java program to find the maximum odd number in an array.



## AIM:
To write a program to find the maximum odd number in an array.


## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Read n elements and store them in the array.
4.Initialize a variable maxOdd with the smallest possible integer value and set found = false.
5.Traverse each element in the array:
6.If the element is odd (arr[i] % 2 != 0)
7.If no odd number was found yet or the current element is greater than maxOdd, update maxOdd.
8.Set found = true.If true then print maxOddElse then print "No odd number found"
```




## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int[] arr=new int[n];
        
        for(int i=0;i<n;i++){
            arr[i]=sc.nextInt();
        }
        int maxOdd=Integer.MIN_VALUE;
        boolean found=false;
        
        for(int i=0;i<n;i++){
            if(arr[i] % 2 != 0){
                if(!found || arr[i] >maxOdd){
                    maxOdd=arr[i];
                }
                found=true;
            }
        }
        if(found){
            System.out.println(maxOdd);
        }
        else{
            System.out.println("No odd number found");
        }
        
    }
}
```






## OUTPUT:

<img width="606" height="608" alt="image" src="https://github.com/user-attachments/assets/d06d40d1-bca8-4558-92ef-4c36f42dbe80" />


## RESULT:

Thus, the program to find the maximum odd number in an array is executed successfully.


# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:

Write a java program to find the index of the last occurrence of a character in a string.

## AIM:

To write a java program to find the index of the last occurrence of a character in a string.


## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Start and read the input string from the user.
4.Read the character whose last occurrence needs to be found
5.Use the lastIndexOf() function on the string to get the index of the last occurrence of the given character.
6.If the returned index is not -1, print the index.
```




## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        String input=sc.nextLine();
        char ch = sc.next().charAt(0);
        int index=input.lastIndexOf(ch);
        if(index != -1){
            System.out.println("Last occurrence of '"+ch+"' is at index: "+index);
        }

    }
}
```






## OUTPUT:

<img width="932" height="322" alt="image" src="https://github.com/user-attachments/assets/d558460a-e7b7-4dcc-8772-fd8d03dc91a4" />


## RESULT:

Thus, the program to find the index of the last occurrence of a character in a string is executed successfully.




