
# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:

Write a java program to find the index of the last occurrence of a character in a string.

## AIM:

To write a java program to find the index of the last occurrence of a character in a string.


## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Start and read the input string from the user.
4.Read the character whose last occurrence needs to be found
5.Use the lastIndexOf() function on the string to get the index of the last occurrence of the given character.
6.If the returned index is not -1, print the index.
```




## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        String input=sc.nextLine();
        char ch = sc.next().charAt(0);
        int index=input.lastIndexOf(ch);
        if(index != -1){
            System.out.println("Last occurrence of '"+ch+"' is at index: "+index);
        }

    }
}
```






## OUTPUT:

<img width="932" height="322" alt="image" src="https://github.com/user-attachments/assets/d558460a-e7b7-4dcc-8772-fd8d03dc91a4" />


## RESULT:

Thus, the program to find the index of the last occurrence of a character in a string is executed successfully.
