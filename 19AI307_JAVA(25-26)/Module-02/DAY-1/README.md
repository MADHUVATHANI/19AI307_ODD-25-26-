# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:

Create a class Course with attributes code, title, credits.

## AIM:

To create a class Course with attributes code, title, credits.

## ALGORITHM :
```
1.	Start the program.
2.Import the necessary package 'java.util'
3.Create two Course objects: c1 and c2.
4.Read the course code, title, and credits for each Course object from the user and store them in object variables.
5.Call the printDetails() method for both objects to display the stored course details.
6.Stop the program.
```




## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.Scanner;
class Course {
    String code;
    String title;
    int credits;

    void printDetails() {
        System.out.println(code + " | " + title + " | " + credits + " credits");
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Course c1 = new Course();
        c1.code = sc.next();
        c1.title = sc.next();
        c1.credits = sc.nextInt();

        Course c2 = new Course();
        c2.code = sc.next();
        c2.title = sc.next();
        c2.credits = sc.nextInt();

        c1.printDetails();
        c2.printDetails();

        sc.close();
    }
}
```






## OUTPUT:

<img width="878" height="327" alt="image" src="https://github.com/user-attachments/assets/7b77cca7-6996-4a41-97f2-77166d011036" />


## RESULT:

Thus, the program to Create a class Course with attributes code, title, credits is executed successfully.

