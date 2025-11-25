# Ex.No:3(E) INNER CLASS

## QUESTION:

<img width="1060" height="181" alt="Screenshot 2025-11-25 114708" src="https://github.com/user-attachments/assets/3adfbe3b-d8ad-47b0-b1a9-60cdfb657257" />


## AIM:

To write a Java program that defines an enum Direction with four constants: NORTH, SOUTH, EAST, WEST, accepts a user input string, converts it into the corresponding enum constant, and displays the selected direction.

## ALGORITHM :

1.Start the program.

2.Define an enum Direction containing:

NORTH, SOUTH, EAST, WEST.

3.In the main() method:

Read a string input from the user (e.g., "North").

Convert the input to uppercase so it matches enum constant format.

Use Direction.valueOf() to convert the string into the enum constant.

4.Print:

You entered direction: <ENUM_VALUE>


5.End program.




## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber:  212223220055
*/

import java.util.Scanner;
enum Direction{
    NORTH,SOUTH,EAST,WEST
}
public class Main{
    public static void main(String[]args){
        Scanner sc=new Scanner(System.in);
        String input=sc.nextLine().trim().toUpperCase();
        try{
            Direction dir = Direction.valueOf(input);
            System.out.println("You entered direction: "+ dir);
        }catch (IllegalArgumentException e){
            System.out.println("Invalid direction entered.");
        }
    }
}
```

## OUTPUT:

<img width="1084" height="242" alt="Screenshot 2025-11-25 114910" src="https://github.com/user-attachments/assets/dc5d28f4-f423-423f-9cb9-6176295c0841" />


## RESULT:

Thus the program has executed successfully to write a Java program that defines an enum Direction with four constants.
