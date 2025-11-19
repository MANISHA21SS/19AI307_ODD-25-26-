# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:

<img width="998" height="362" alt="Screenshot 2025-11-19 102317" src="https://github.com/user-attachments/assets/f0b7f80e-1240-4333-a487-435c73b624df" />


## AIM:

To write a Java program that simulates the behavior of a magical elevator based on the following rules:

If the floor number is divisible by both 3 and 5, print "Skipped".

If the floor number is divisible by 3 only, print "Beware!".

If the floor number is divisible by 5 only, print "Blessings!".

Otherwise, print "Floor {number}".

## ALGORITHM :

1.Start

2.Read the floor number as input.

3.Check if the number is divisible by both 3 and 5

4.If true → print "Skipped".

5.Else check if the number is divisible by 3 only

6.If true → print "Beware!".

7.Else check if the number is divisible by 5 only

8.If true → print "Blessings!".

Else

Print "Floor {number}".

9.Stop



## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber: 212223220055
*/

import java.util.Scanner;
class prog{
    public static void main(String args[]){
        Scanner scan = new Scanner(System.in);
        int floor =scan.nextInt();
        if(floor%3==0 && floor%5==0){
            System.out.println("Skipped");
        }else if(floor%3==0){
            System.out.println("Beware!");
        }else if(floor%5==0){
            System.out.println("Blessings!");
        }else{
            System.out.println("Floor "+floor);
        }
    }
}
```


## OUTPUT:

<img width="1285" height="402" alt="Screenshot 2025-11-19 102607" src="https://github.com/user-attachments/assets/ca80d500-0558-4d65-ac7b-c0948c38501c" />



## RESULT:

Thus, the program writes a Java program that simulates the behavior of a magical elevator based on the rules.
