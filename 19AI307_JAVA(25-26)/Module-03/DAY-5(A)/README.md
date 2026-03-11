# Ex.No:3(E) INNER CLASS

## QUESTION:
Write an enum VehicleType (CAR, BIKE, BUS) with a constructor that takes number of wheels. Print wheel count for each.



## AIM:
To write an enum VehicleType (CAR, BIKE, BUS) with a constructor that takes number of wheels. Print wheel count for each.



## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Convert the input to uppercase and try to match it with an enum constant using valueOf().
4.	If the input matches a valid enum, retrieve the number of wheels using getWheels().
5.	Display the vehicle name and its wheel count.
6.	If the input doesn’t match any enum, show an error message, then stop.





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.Scanner;

enum VehicleType {
    CAR(4),
    BIKE(2),
    BUS(6);

    private int wheels;

    VehicleType(int wheels) {
        this.wheels = wheels;
    }

    public int getWheels() {
        return wheels;
    }
}

public class VehicleEnumDemo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.next().toUpperCase();

        try {
            VehicleType vehicle = VehicleType.valueOf(input);
            System.out.println(vehicle + " has " + vehicle.getWheels() + " wheels.");
        } catch (IllegalArgumentException e) {
            System.out.println("Invalid vehicle type entered.");
        }

        sc.close();
    }
}
```






## OUTPUT:

<img width="803" height="360" alt="image" src="https://github.com/user-attachments/assets/c9826371-743f-42a3-90c0-8737cf6d65cd" />


## RESULT:

Thus, the program to print wheel count for each is executed successfully.


