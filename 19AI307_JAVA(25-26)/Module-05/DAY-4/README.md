# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for determine the priority and name of the current thread.

Note : Read the threadname from the User

## AIM:

To Write a java program for determine the priority and name of the current thread.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a thread name from the user using Scanner.
4.	Get the reference of the current running thread using Thread.currentThread().
5.	Change the name of the current thread to the user-provided name.
6.	Retrieve the current thread’s priority using getPriority().
7.	Print the thread’s priority, updated name, and full thread information.







## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.Scanner;

public class CurrentThreadInfo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();

        Thread currentThread = Thread.currentThread();

        currentThread.setName(threadName);

        int priority = currentThread.getPriority();

        System.out.println("Priority of Thread: " + priority);
        System.out.println("Name of Thread: " + currentThread.getName());
        System.out.println(currentThread);

        sc.close();
    }
}
```






## OUTPUT:

<img width="810" height="216" alt="image" src="https://github.com/user-attachments/assets/ca622a76-977c-4f2b-adbd-152f41676c8d" />


## RESULT:

Thus, the program to determine the priority and name of the current thread is executed successfully.

