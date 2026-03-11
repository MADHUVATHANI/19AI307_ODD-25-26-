# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Rectangle with private instance variables length and width. Provide public getter and setter methods to access and modify these variables

## AIM:
To Write a Java program to create a class called Rectangle with private instance variables length and width.
## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Create an object of the Rectangle class.
4.Use the setter methods setLength() and setWidth() to store the input values in the object.
5.Retrieve the stored values using getLength() and getWidth().
6.Display the length and width, then stop the program.
```




## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.Scanner;
class Rectangle {
    private double length;
    private double width;

    public double getLength() {
        return length;
    }
    public void setLength(double length) {
        this.length = length;
    }

    public double getWidth() {
        return width;
    }
    public void setWidth(double width) {
        this.width = width;
    }

    public double calculateArea() {
        return length * width;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        Rectangle rect = new Rectangle();

        double length = scanner.nextDouble();
        rect.setLength(length);

        double width = scanner.nextDouble();
        rect.setWidth(width);

        System.out.println("Length: " + rect.getLength());
        System.out.println("Width: " + rect.getWidth());

    }
}
```






## OUTPUT:

<img width="618" height="461" alt="image" src="https://github.com/user-attachments/assets/217853f0-7875-4de6-a604-6e59602014be" />


## RESULT:

Thus, the program to create a class called Rectangle with private instance variables length and width is executed successfully.
