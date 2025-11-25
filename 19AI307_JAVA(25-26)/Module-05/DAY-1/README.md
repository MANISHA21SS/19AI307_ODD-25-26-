# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:

<img width="818" height="171" alt="Screenshot 2025-11-25 145314" src="https://github.com/user-attachments/assets/9dbfa24d-43fc-4328-a856-9fa145e23902" />


## AIM:

To write a Java program that reads user input from the keyboard using InputStreamReader (wrapped inside a BufferedReader for efficient reading), and then display a personalized greeting message to the user.

## ALGORITHM :

1.Start

2.Create an InputStreamReader object to read bytes from keyboard (System.in) and convert them into characters.

3.Wrap it inside a BufferedReader to enable reading a full line of text.

4.Display a prompt asking the user to enter their name.

5.Read the input string using readLine() method.

6.Store the entered name.

7.Display the message:
"Hello, [name]!"

8.End


## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber:  212223220055
*/

import java.io.*;

public class ReadInputExample {
    public static void main(String[] args) {
        try {
            InputStreamReader isr = new InputStreamReader(System.in);
            BufferedReader br = new BufferedReader(isr);
            String name = br.readLine();

            System.out.println("Hello, " + name + "!");
        } catch (IOException e) {
            System.out.println("An error occurred while reading input.");
        }
    }
}

```

## OUTPUT:

<img width="888" height="207" alt="Screenshot 2025-11-25 145507" src="https://github.com/user-attachments/assets/36e12847-ca91-4f2d-af8b-87c457d98391" />


## RESULT:

Thus the program has executed successfully to write a Java program that reads user input from the keyboard using InputStreamReader.
