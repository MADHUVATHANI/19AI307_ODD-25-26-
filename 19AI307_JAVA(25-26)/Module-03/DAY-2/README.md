# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator with: area(int side) for square ,area(int length, int breadth) for rectangle,area(double radius) for circle

## AIM:

To Write a Java program that calculates the area of different shapes using method overloading.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an object of the AreaCalculator class.
4.	Call the overloaded method area(int side) to calculate and print the area of the square.
5.	Call the overloaded method area(int length, int breadth) to calculate and print the area of the rectangle.
6.	Call the overloaded method area(double radius) to calculate and print the area of the circle, then stop.





## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.Scanner;

class AreaCalculator {

    void area(int side) {
        int squareArea = side * side;
        System.out.println("Area of square: " + squareArea);
    }

    void area(int length, int breadth) {
        int rectangleArea = length * breadth;
        System.out.println("Area of rectangle: " + rectangleArea);
    }

    void area(double radius) {
        double circleArea = Math.PI * radius * radius;
        System.out.println("Area of circle: " + circleArea);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        AreaCalculator obj = new AreaCalculator();

        int side = sc.nextInt();
        obj.area(side);

        int length = sc.nextInt();
        int breadth = sc.nextInt();
        obj.area(length, breadth);

        double radius = sc.nextDouble();
        obj.area(radius);

        sc.close();
    }
}
```






## OUTPUT:

<img width="867" height="488" alt="image" src="https://github.com/user-attachments/assets/4b8db958-eade-4915-9999-a4981aa97ed7" />


## RESULT:
Thus, the program to calculates the area of different shapes using method overloading is executed successfully.

