# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:

<img width="936" height="177" alt="Screenshot 2025-11-19 103455" src="https://github.com/user-attachments/assets/555283a7-d246-4455-b20a-6ee75ec4e4d9" />


## AIM:

To write a Java program that takes a string as input and prints its reverse.

## ALGORITHM :

1.Start

2.Read the input string from the user.

3.Initialize an empty string rev = "".

4.Loop through the original string from last character to first.

5.Append each character to rev.

6.Print rev as the reversed string.

7.Stop




## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber: 212223220055 
*/
import java.util.Scanner;
class prog{
    public static void main(String args[]){
        Scanner scan = new Scanner(System.in);
        String str = scan.nextLine();
        String reversed = new StringBuilder(str).reverse().toString();
        System.out.println("Reversed string: "+reversed);
        
    }
}
```



## OUTPUT:

<img width="1293" height="349" alt="Screenshot 2025-11-19 103654" src="https://github.com/user-attachments/assets/acade8cf-da08-4479-946d-79d073852655" />



## RESULT:
Thus, the program writes a Java program that takes a string as input and prints its reverse.
