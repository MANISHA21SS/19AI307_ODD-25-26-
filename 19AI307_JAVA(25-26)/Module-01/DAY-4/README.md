# Ex.No:1(D) ARRAYS

## QUESTION:

<img width="1134" height="327" alt="Screenshot 2025-11-19 103134" src="https://github.com/user-attachments/assets/992eb3dd-2933-48ec-8aea-1dcb82682e54" />


## AIM:

To write a Java program that reads an array of numbers and calculates the average of all elements.

## ALGORITHM :

1.Start

2.Read the total number of elements n.

3.Create an array of size n.

4.Read all n elements from the user.

5.Initialize sum = 0.

6.Use a for loop to add each element to sum.

7.Compute average as:
average = sum / n

8.Print the average.

9.Stop





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber: 212223220055
*/
import java.util.Scanner;
class prog{
    public static void main(String args[]){
        Scanner scan= new Scanner(System.in);
        int n = scan.nextInt();
        int[] arr = new int[n];
        int sum =0;
        for(int i =0;i<n;i++){
            arr[i]=scan.nextInt();
            sum+=arr[i];
        }
        double average = (double) sum/n;
        System.out.println(String.format("The average of elements is %.2f", average));

    }
}
```


## OUTPUT:

<img width="1281" height="572" alt="Screenshot 2025-11-19 103343" src="https://github.com/user-attachments/assets/1de55800-5913-479e-a8b7-9aabb646d5cb" />



## RESULT:

Thus, the program writes a Java program that reads an array of numbers and calculates the average of all elements.

