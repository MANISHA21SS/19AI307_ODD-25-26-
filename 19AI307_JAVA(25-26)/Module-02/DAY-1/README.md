# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:

<img width="1111" height="228" alt="Screenshot 2025-11-19 103810" src="https://github.com/user-attachments/assets/5e88e70e-c11a-466c-b1fe-d52f396cecbc" />

## AIM:

To create a Vehicle class with attributes number, type, and owner, and write a Java program that reads vehicle details and prints them in a formatted manner.

## ALGORITHM :

1.Start

2.Create a Vehicle class with:

String number

String type

String owner

3.Create a constructor to initialize these attributes.

4.In the main method:

Read inputs for two vehicles.

5.Create two Vehicle objects.

6.Print the vehicle details in the format:
number | type | owner

7.Stop





## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber: 212223220055
*/
import java.util.Scanner;
class Vehicle{
       String number;
       String type;
       String owner;
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Vehicle v1 = new Vehicle();
        v1.number = sc.next();
        v1.type = sc.next();
        v1.owner = sc.next();

        Vehicle v2 = new Vehicle();
        v2.number = sc.next();
        v2.type = sc.next();
        v2.owner = sc.next();

        System.out.println(v1.number + " | " + v1.type + " | " + v1.owner);
        System.out.println(v2.number + " | " + v2.type + " | " + v2.owner);

        sc.close();
    }
}

```


## OUTPUT:

<img width="1225" height="343" alt="Screenshot 2025-11-19 103954" src="https://github.com/user-attachments/assets/45030057-441f-4ad4-b595-1c3f3696e154" />



## RESULT:

Thus, the program writes a Java program that reads vehicle details and prints them in a formatted manner.
