# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".

## AIM:

To Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".
## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Call the static method Calculator.info() to print a message.
4. Create an object of the Calculator class.
5. Call the instance method add(a, b) using the object to compute the sum.
6. Print the result and stop the program.
```




## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.Scanner;

class Calculator {
    public int add(int a, int b) {
        return a + b;
    }

    public static void info() {
        System.out.println("Calculator is ready");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int num1 = sc.nextInt();
        int num2 = sc.nextInt();

        Calculator.info();

        Calculator calc = new Calculator();
        int sum = calc.add(num1, num2);

        System.out.println("Sum: " + sum);
    }
}
```






## OUTPUT:

<img width="656" height="393" alt="image" src="https://github.com/user-attachments/assets/3adde931-0cd4-42c3-ae1a-199509830954" />


## RESULT:

Thus, the program to Create a class Calculator that says "Calculator is ready is executed successfully.
