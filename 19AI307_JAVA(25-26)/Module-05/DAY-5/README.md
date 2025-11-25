# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:

<img width="922" height="313" alt="Screenshot 2025-11-25 151937" src="https://github.com/user-attachments/assets/0c227f0f-e1e1-46ce-aeef-ff44145b2cf9" />


## AIM:

To write a Java program that creates two threads which print "Hello" and "World" alternately using synchronized blocks to ensure proper coordination and avoid race conditions.

## ALGORITHM :

1.Start

2.Create a shared lock object (e.g., Object lock = new Object()) to synchronize threads.

3.Define a shared flag (e.g., boolean helloTurn = true) to indicate which thread’s turn it is.

4.Create Thread1 to print "Hello":

Use a synchronized block on the lock object.

Inside a loop for n times:

Wait if it is not Hello’s turn (while(!helloTurn) lock.wait()).

Print "Hello".

Set helloTurn = false.

Notify the other thread (lock.notify()).

5.Create Thread2 to print "World":

Use a synchronized block on the lock object.

Inside a loop for n times:

Wait if it is not World’s turn (while(helloTurn) lock.wait()).

Print "World".

Set helloTurn = true.

Notify the other thread (lock.notify()).

6.Start both threads.

7.Wait for both threads to finish using join().

8.End





## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber: 212223220055
*/

import java.util.Scanner;

public class AlternateHelloWorld {

    private static final Object lock = new Object();
    private static boolean helloTurn = true;

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();  

        Thread t1 = new Thread(() -> {
            for (int i = 0; i < n; i++) {
                synchronized (lock) {
                    while (!helloTurn) {
                        try { lock.wait(); } catch (Exception e) {}
                    }
                    System.out.println("Hello");
                    helloTurn = false;
                    lock.notify();
                }
            }
        });

        Thread t2 = new Thread(() -> {
            for (int i = 0; i < n; i++) {
                synchronized (lock) {
                    while (helloTurn) {
                        try { lock.wait(); } catch (Exception e) {}
                    }
                    System.out.println("World");
                    helloTurn = true;
                    lock.notify();
                }
            }
        });

        t1.start();
        t2.start();
    }
}

```

## OUTPUT:

<img width="1089" height="701" alt="Screenshot 2025-11-25 152234" src="https://github.com/user-attachments/assets/c20f5ae6-bfd2-4708-bbd6-542d1bf19b02" />



## RESULT:
Thus the program has executed successfully to write a Java program that creates two threads which print "Hello" and "World" alternately using synchronized blocks to ensure proper coordination and avoid race conditions.


