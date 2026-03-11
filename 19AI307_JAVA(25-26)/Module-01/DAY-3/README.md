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

