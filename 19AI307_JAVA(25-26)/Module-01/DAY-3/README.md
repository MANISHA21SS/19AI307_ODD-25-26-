# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:

<img width="1282" height="239" alt="Screenshot 2025-11-19 102810" src="https://github.com/user-attachments/assets/19de3f20-4c9a-41e2-8475-3df370201f2b" />


## AIM:

To write a Java program that calculates the factorial of a given number using a for loop.

## ALGORITHM :

1.Start

2.Read an integer n from the user.

3.Initialize a variable fact = 1.

4.Use a for loop from i = 1 to n:

5.Multiply fact = fact * i.

6.After the loop ends, print "Factorial of n is: fact"

7.Stop




## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Manisha selvakumari.S.S. 
RegisterNumber: 212223220055
*/

import java.util.Scanner;
class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        long factorial = 1; 
        for (int i = 1; i <= n; i++) {
            factorial *= i; 
        }

        System.out.println("Factorial of " + n + " is: " + factorial);
    }
}

```

## OUTPUT:

<img width="1283" height="345" alt="image" src="https://github.com/user-attachments/assets/03979d86-1ed1-427b-b349-bc894647c6bb" />


## RESULT:

Thus, the program writes a Java program that calculates the factorial of a given number using a for loop.

