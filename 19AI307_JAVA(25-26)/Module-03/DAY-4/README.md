# Ex.No:3(D)    INTERFACE 

## QUESTION:
You’re developing ZoomCarGo v3, a super-smart dispatch system that helps users book a ride based on their travel distance and budget.
The system must:
Allow user to input travel distance and budget.
Show only the available rides that can handle the distance and fit within the budget.
If multiple rides are available, pick the cheapest one and book it.
If no ride matches, show a proper error message.

Ride Type	Max Distance	Price/km	Class
Auto	8 km	₹10/km	AutoRide
Bike	15 km	₹15/km	BikeRide
Cab	Unlimited	₹20/km	CabRide


## AIM:

To build a ride-selection system that filters rides based on distance and budget, then automatically books the cheapest valid option.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a list of ride options: AutoRide, BikeRide, and CabRide, each with their max distance and price per km.
4.	For each ride, check if it is available (distance within limit and fare ≤ budget); if yes, calculate its fare.
5.	Among all available rides, select the ride with the lowest fare.
6.	If a suitable ride exists, display the booked ride and fare; otherwise, print that no rides match the requirements, then stop.





## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.*;

abstract class Ride {
    String name;
    int maxDistance;
    int pricePerKm;

    Ride(String name, int maxDistance, int pricePerKm) {
        this.name = name;
        this.maxDistance = maxDistance;
        this.pricePerKm = pricePerKm;
    }

    boolean isAvailable(int distance, int budget) {
        int totalFare = distance * pricePerKm;
        return (maxDistance == -1 || distance <= maxDistance) && totalFare <= budget;
    }

    int calculateFare(int distance) {
        return distance * pricePerKm;
    }
}

class AutoRide extends Ride {
    AutoRide() {
        super("AutoRide", 8, 10);
    }
}

class BikeRide extends Ride {
    BikeRide() {
        super("BikeRide", 15, 15);
    }
}

class CabRide extends Ride {
    CabRide() {
        super("CabRide", -1, 20); 
    }
}

public class ZoomCarGoV3 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int distance = sc.nextInt();
        int budget = sc.nextInt();

        List<Ride> rides = new ArrayList<>();
        rides.add(new AutoRide());
        rides.add(new BikeRide());
        rides.add(new CabRide());

        Ride bestRide = null;
        int minFare = Integer.MAX_VALUE;

        for (Ride ride : rides) {
            if (ride.isAvailable(distance, budget)) {
                int fare = ride.calculateFare(distance);
                if (fare < minFare) {
                    minFare = fare;
                    bestRide = ride;
                }
            }
        }

        if (bestRide != null) {
            System.out.println(bestRide.name + " booked for " + distance + " km. Fare: ₹" + minFare + ".");
        } else {
            System.out.println("No rides available for your distance and budget.");
        }

        sc.close();
    }
}
```






## OUTPUT:

<img width="961" height="288" alt="image" src="https://github.com/user-attachments/assets/82a0f720-1396-4eb7-b186-6059c4bd2e46" />


## RESULT:

Thus, the program to build a ride-selection system that filters rides based on distance and budget, then automatically books the cheapest valid option is executed successfully.

