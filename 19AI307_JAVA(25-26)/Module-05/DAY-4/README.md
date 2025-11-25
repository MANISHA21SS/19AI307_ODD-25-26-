# Ex.No:5(D) THREAD PRIORITY

## QUESTION:

<img width="1027" height="309" alt="Screenshot 2025-11-25 151244" src="https://github.com/user-attachments/assets/90b73d5e-cb61-4ee1-b0dc-eab851b3a4b3" />


## AIM:

To write a Java program that sets the name of the current thread based on user input and sets its priority to 2.

## ALGORITHM :

1.Start

2.Import the java.util.Scanner class to read input from the user.

3.Create a Scanner object to read the thread name from the user.

4.Get the current thread using Thread.currentThread().

5.Set the priority of the current thread to 2 using setPriority(2).

6.Set the name of the current thread to the input name using setName(threadName).

7.Display the priority of the thread using getPriority().

8.Display the name of the thread using getName().

9.Display the thread details directly by printing the thread object.

10.End





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber: 212223220055 
*/

import java.util.Scanner;

public class ThreadSetDetails {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

      
        String threadName = sc.nextLine();

        Thread currentThread = Thread.currentThread();

        currentThread.setName(threadName);
        currentThread.setPriority(2);

        System.out.println("Priority of Thread: " + currentThread.getPriority());
        System.out.println("Name of Thread: " + currentThread.getName());
        System.out.println(currentThread);
    }
}

```


## OUTPUT:

<img width="946" height="203" alt="Screenshot 2025-11-25 151556" src="https://github.com/user-attachments/assets/3cc6e2a9-c763-4c65-8d4d-3c3d2c96f536" />


## RESULT:
Thus the program has executed successfully to write a Java program that sets the name of the current thread based on user input and sets its priority to 2.


