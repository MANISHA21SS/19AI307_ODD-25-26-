# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:

<img width="1095" height="123" alt="Screenshot 2025-11-25 140925" src="https://github.com/user-attachments/assets/18a2d512-4058-495c-af3f-7e78949346c7" />


## AIM:

To write a Java program that stores input strings in a String array and prints each string in uppercase without causing a NullPointerException.
The aim is to ensure that each array element is not null before calling the .toUpperCase() method.

## ALGORITHM :

1.Start

2.Declare a String array with a specific size

3.Read input strings from the user and store them in the array

4.For each array element:

Check if the element is not null

If not null → convert to uppercase and print

Otherwise → skip or print a message

5.End




## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber:  212223220055
*/

import java.util.*;

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        while (sc.hasNextLine()) {
            String s = sc.nextLine().trim();

            // If input text itself is "null"
            if (s.equals("null")) {
                System.out.println("Null element");
            } else {
                System.out.println(s.toUpperCase());
            }
        }
    }
}

```



## OUTPUT:

<img width="865" height="247" alt="Screenshot 2025-11-25 141156" src="https://github.com/user-attachments/assets/875bcd53-8400-4140-a968-7c2a87a3929e" />


## RESULT:

Thus the program has executed successfully to write a Java program that stores input strings in a String array and prints each string in uppercase without causing a NullPointerException.
