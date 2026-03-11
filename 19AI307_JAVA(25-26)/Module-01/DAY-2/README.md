
# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
A train company charges tickets based on age and travel class:

Children (<12): ₹5 per km (any class)

Adults (12–60):

Sleeper: ₹10/km

AC: ₹15/km

Seniors (>60): ₹7/km (any class)

Task: Accept age, distance and travel class (1 for Sleeper, 2 for AC)(follow the same order to get the inputs). Calculate fare.

For example:

Input	
5
100
Result
500



## AIM:

To write a program that accepts the age, distance, and travel class (1 for Sleeper, 2 for AC) and calculates the train fare based on age-wise and class-wise fare rules.

## ALGORITHM :
```
1.Start and read the inputs: age, distance, and travel class.
2.Determine the rate per km based on age and class conditions.
3.If age < 12, set rate = 5;
   else if age 12–60, set rate = 10 for Sleeper or 15 for AC;
   else if age > 60, set rate = 7.
4.Calculate the fare using: fare = distance × rate.
5.Display the total fare and Stop.
```




## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: Madhuvathani v
RegisterNumber:  212223040107
*/
```

```
import java.util.Scanner;

public class TrainFare {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int age = sc.nextInt();
        int distance = sc.nextInt();

        int farePerKm=0;;

        if (age < 12) {
            farePerKm = 5;
        } else if (age > 60) {
            farePerKm = 7;
        } else { 
            int travelClass = sc.nextInt();
            if (travelClass == 1) {
                farePerKm = 10;
            } else if (travelClass == 2) {
                farePerKm = 15;
            } else {
                System.out.println("Invalid class");
                return;
            }
        }

        int totalFare = farePerKm * distance;
        System.out.println(totalFare);
    }
}
```


## OUTPUT:

<img width="652" height="356" alt="image" src="https://github.com/user-attachments/assets/492431f7-c261-4417-aecd-114541a862fd" />


## RESULT:

Thus, a java program to calculates the train fare based on age-wise and class-wise fare rules is executed successfully.

