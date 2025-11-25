# Ex.No:3(F) WRAPPER CLASS

## QUESTION:

<img width="829" height="184" alt="Screenshot 2025-11-25 115116" src="https://github.com/user-attachments/assets/af4022aa-02aa-44ab-adbe-3a3f9c77b8c7" />


## AIM:

To write a Java program that checks whether a given number is a prime number using wrapper classes (e.g., Integer), demonstrating type conversion and usage of wrapper class methods.

## ALGORITHM :

1.Start the program.

2.Read the input number as a string.

3.Convert the string to an Integer object using:

Integer num = Integer.valueOf(input);


If num is ≤ 1, it is not prime.

For numbers greater than 1:

Loop from i = 2 to sqrt(num)

4.If num % i == 0, then the number is not prime

Break the loop.

5.If no divisor is found, the number is prime.

6.Print:

"X is a prime number."
or

"X is not a prime number."

7.End program.





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber: 212223220055 
*/

import java.util.Scanner;
public class PrimeCheck{
    public static void main(String[]args){
        Scanner sc = new Scanner(System.in);
        int num=sc.nextInt();
        Integer number = Integer.valueOf(num);
        if(isPrime(number)){
            System.out.println(number + " is a prime number.");
        }else{
            System.out.println(number + " is not a prime number.");
        }
    }
    public static boolean isPrime(Integer n){
        if(n<=1) return false;
        for(int i=2;i<=Math.sqrt(n);i++){
            if(n%i==0) return false;
        }
        return true;
    }
}
```


## OUTPUT:

<img width="1134" height="249" alt="Screenshot 2025-11-25 115327" src="https://github.com/user-attachments/assets/434575eb-58b0-4394-a2fb-77e54db82e8e" />



## RESULT:

Thus the program has executed successfully to write a Java program that checks whether a given number is a prime number using wrapper classes .
