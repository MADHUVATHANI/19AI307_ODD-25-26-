# Ex.No:2(B) METHODS

## QUESTION:

Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).


## AIM:

To Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).


## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Create an object of the MathUtil class.
4.Call the cube() method using the object, passing the input value.
5.The cube() method internally calls square() to compute:cube = x × (x × x).
6.Print the cube value and stop.
```




## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.Scanner;

class MathUtil {

    int square(int x) {
        return x * x;
    }

    int cube(int x) {
        return x * square(x);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        int num = scanner.nextInt();  

        MathUtil util = new MathUtil();
        int result = util.cube(num);  

        System.out.println(result);   

        scanner.close();
    }
}
```






## OUTPUT:

<img width="392" height="242" alt="image" src="https://github.com/user-attachments/assets/e5a3ea04-0840-4c35-ae01-f0290c43eea3" />


## RESULT:

Thus, the program to  a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x) executed successfully.
