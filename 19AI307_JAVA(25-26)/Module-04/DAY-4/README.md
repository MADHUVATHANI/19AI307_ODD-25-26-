# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:

Create a program that loads an operating system shell using the Factory Pattern. Based on user input, return a shell object: windows, linux, mac.


## AIM:

To create a program that loads an operating system shell using the Factory Pattern. Based on user input, return a shell object: windows, linux, mac.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the OS name from the user.
4.	Use OSFactory.getOS() to create the appropriate OS object based on the input.
5.	If a valid OS object is returned, call its loadShell() method.
6.	If the input does not match any OS type, display "Invalid OS" message.





## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.Scanner;

interface OperatingSystem {
    void loadShell();
}


class Windows implements OperatingSystem {
    public void loadShell() {
        System.out.println("Loading Windows Shell...");
    }
}

class Linux implements OperatingSystem {
    public void loadShell() {
        System.out.println("Loading Linux Shell...");
    }
}

class Mac implements OperatingSystem {
    public void loadShell() {
        System.out.println("Loading Mac Shell...");
    }
}

class OSFactory {
    public static OperatingSystem getOS(String type) {
        if (type.equals("Windows")) {
            return new Windows();
        } else if (type.equals("Linux")) {
            return new Linux();
        } else if (type.equals("Mac")) {
            return new Mac();
        } else {
            return null; 
        }
    }
}

public class ShellLoader {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
       
        String input = sc.nextLine();

        OperatingSystem os = OSFactory.getOS(input);

        if (os != null) {
            os.loadShell();
        } else {
            System.out.println("Invalid OS: " + input);
        }

        sc.close();
    }
}
```






## OUTPUT:

<img width="673" height="418" alt="image" src="https://github.com/user-attachments/assets/3837199b-482d-4131-bd9f-7ea89a7d59c7" />


## RESULT:

Thus, the program to loads an operating system shell using the Factory Pattern is executed successfully.

