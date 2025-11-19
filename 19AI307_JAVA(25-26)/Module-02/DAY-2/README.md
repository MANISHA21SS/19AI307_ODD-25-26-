# Ex.No:2(B) METHODS

## QUESTION:

<img width="1076" height="372" alt="Screenshot 2025-11-19 104155" src="https://github.com/user-attachments/assets/e5779a74-f98c-42d1-be3a-f5e1ced2ea78" />


## AIM:

To write a Java program that takes the radius of a circle as input, calculates the area using a separate method, and prints the area using another method.

## ALGORITHM :

1.Start

2.Create a method double getArea(double r):

3.Calculate area using formula
area = 3.14 × r × r

4.Return the area.

5.Create a method void printArea(double area):

6.Print the area value.

7.In main:

Read radius from user.

8.Call getArea() to compute area.

9.Call printArea() to display area.

10.Stop





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber: 212223220055  
*/
import java.util.Scanner;
public class CircleArea{
     static double getArea(double r){
         return 3.14*r*r;
     }
     static void printArea(double area){
          System.out.printf("%.2f\n",area);
     }
     public static void main(String[]args){
       Scanner scan = new Scanner(System.in);
        double radius = scan.nextDouble();
        double area = getArea(radius);
        printArea(area);
        scan.close();
   }
}
```


## OUTPUT:

<img width="1235" height="269" alt="Screenshot 2025-11-19 104351" src="https://github.com/user-attachments/assets/e063bbcd-cc78-40fc-890d-9d23d866bcd7" />


## RESULT:

Thus, the program writes a Java program that takes the radius of a circle as input, calculates the area using a separate method, and prints the area using another method.
