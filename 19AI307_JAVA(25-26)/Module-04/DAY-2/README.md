# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:

<img width="1218" height="779" alt="Screenshot 2025-11-25 141807" src="https://github.com/user-attachments/assets/33746384-1d0c-443e-b505-728a8805ddf6" />


## AIM:

To create a program that ensures only one instance of Print Spooler Manager exists using the Singleton design pattern, and to maintain a shared job count across all job submissions from different departments.

## ALGORITHM :

1.Start

2.Create a PrintSpooler class with:

A private static instance of itself

A private constructor to prevent external creation

A public static getInstance() method to return the single instance

A job counter to track number of print jobs

A method addJob(String dept) to increment and print the count

3.In the main method:

Read number of print jobs n

Loop n times reading department names

For each input, get the singleton instance and call addJob()

4.End




## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Manisha selvakumari.S.S.
RegisterNumber: 212223220055
*/

import java.util.Scanner;

class PrintSpoolerManager {
    private static PrintSpoolerManager instance; 
    private int jobCount;

    private PrintSpoolerManager() {
        jobCount = 0;
    }

    public static PrintSpoolerManager getInstance() {
        if (instance == null) {
            instance = new PrintSpoolerManager();
        }
        return instance;
    }

    public void submitJob(String department) {
        jobCount++;
        System.out.println(department + " submitted a print job. Total Jobs in Queue: " + jobCount);
    }
}

public class SingletonPrintQueue {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = Integer.parseInt(sc.nextLine());

        PrintSpoolerManager manager = PrintSpoolerManager.getInstance();

        for (int i = 0; i < n; i++) {
            String department = sc.nextLine();
            manager.submitJob(department);
        }

        sc.close();
    }
}

```

## OUTPUT:

<img width="1188" height="443" alt="Screenshot 2025-11-25 142015" src="https://github.com/user-attachments/assets/6dea849b-fade-4cdf-86b4-9a62931f16f6" />


## RESULT:

Thus the program has executed successfully to create a program that ensures only one instance of Print Spooler Manager exists using the Singleton design pattern.
