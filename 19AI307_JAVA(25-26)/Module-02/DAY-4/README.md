# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a class that uses a constructor to count the number of objects created.


## AIM:
To write a class that uses a constructor to count the number of objects created.



## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Initialize a static variable count to 0 (used to track number of objects).
4.Run a loop from 0 to n−1.
5.Inside each loop iteration, create a new object of class prog, and the constructor increments count.
6.After the loop ends, display the total count of created objects and stop.
```




## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.Scanner;

class prog {
    static int count = 0;

    prog() {
        count++;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();   

        for (int i = 0; i < n; i++) {
            new prog();
        }

        System.out.println("Number of objects created: " + count);

        sc.close();
    }
}
```






## OUTPUT:

<img width="808" height="332" alt="image" src="https://github.com/user-attachments/assets/5247c082-c2b1-4400-9aee-873510d83313" />


## RESULT:

Thus, the program to count the number of objects created is executed successfully.

