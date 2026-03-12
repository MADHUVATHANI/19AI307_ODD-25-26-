# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Build a simple Air Traffic Control System where multiple Airplane objects request landing through a central mediator.

## AIM:

To Build a simple Air Traffic Control System where multiple Airplane objects request landing through a central mediator.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create AirTrafficControl object based on runway mode.
4.	Create each Airplane object by reading airplane names and linking them to the control tower.
5.	Each airplane requests landing through the control tower.
6.	Control tower decides:If multiple landings allowed then all land.If single landing allowed then only first lands, others are denied.





## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.*;

class AirTrafficControl {
    private final boolean allowMultiple; 

    private boolean firstLanded; 

    public AirTrafficControl(boolean runwayFreeInitially) {
        this.allowMultiple = runwayFreeInitially;
        this.firstLanded = false;
    }

    public void requestLanding(Airplane airplane) {
        if (allowMultiple) {
            System.out.println(airplane.getName() + " granted landing.");
            airplane.land();
        } else {
            if (!firstLanded) {
                System.out.println(airplane.getName() + " granted landing.");
                airplane.land();
                firstLanded = true;
            } else {
                System.out.println(airplane.getName() + " denied landing. Runway busy.");
            }
        }
    }
}

class Airplane {
    private String name;
    private AirTrafficControl control;

    public Airplane(String name, AirTrafficControl control) {
        this.name = name;
        this.control = control;
    }

    public String getName() {
        return name;
    }

    public void requestLanding() {
        control.requestLanding(this);
    }

    public void land() {
        System.out.println(name + " landed successfully.");
    }
}

public class AirTrafficSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        while (sc.hasNextInt()) {
            int n = sc.nextInt();
            if (!sc.hasNext()) break;
            boolean runwayFree;
            try {
                runwayFree = sc.nextBoolean();
            } catch (InputMismatchException e) {
                sc.next(); 
                break;
            }
            sc.nextLine(); 

            AirTrafficControl control = new AirTrafficControl(runwayFree);
            List<Airplane> planes = new ArrayList<>();

            for (int i = 0; i < n; i++) {
                if (!sc.hasNextLine()) break;
                String name = sc.nextLine();
                planes.add(new Airplane(name, control));
            }

            for (Airplane p : planes) {
                p.requestLanding();
            }
        }

        sc.close();
    }
}
```






## OUTPUT:

<img width="997" height="640" alt="image" src="https://github.com/user-attachments/assets/0dfd5285-fbfc-420c-bc79-c77f5eb43fba" />


## RESULT:

Thus, the program to build a simple Air Traffic Control System

