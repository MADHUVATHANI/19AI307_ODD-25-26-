# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to find the square root of a number using Double wrapper class.



## AIM:
To write a Java program to find the square root of a number using Double wrapper class.



## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Use the built-in Math.sqrt() function to compute the square root of the given number.
4.	Store the result in a variable.
5.	Display the original number and its square root.
6.	Stop the program





## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.Scanner;

public class SquareRootDemo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double num = sc.nextDouble();

        double sqrt = Double.valueOf(Math.sqrt(num));

        System.out.println("Square root of " + num + " is: " + sqrt);

        sc.close();
    }
}
```






## OUTPUT:

<img width="840" height="357" alt="image" src="https://github.com/user-attachments/assets/ee9d2d55-b671-4b95-b6e4-1bef750955d8" />


## RESULT:

Thus,the program to find the square root of a number using Double wrapper class is executed successfully.



