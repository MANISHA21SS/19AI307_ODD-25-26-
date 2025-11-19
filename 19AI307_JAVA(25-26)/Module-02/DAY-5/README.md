# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:

<img width="1227" height="233" alt="Screenshot 2025-11-19 105235" src="https://github.com/user-attachments/assets/9b665ca7-0a98-4ec1-be9c-a29c00444d7a" />


## AIM:

To create a Student class in Java with variables name and rollNumber, define a method setDetails to assign values to these variables, and display them.

## ALGORITHM :

1.Start the program.

2.Create a class Student.

3.Declare instance variables name (String) and rollNumber (int).

4.Define a method setDetails(String name, int rollNumber) to assign values to the variables.

5.Define a method display() to print the name and roll number.

6.Create a Main class with the main method.

7.Take input from the user for the student name and roll number.

8.Create an object of the Student class.

9.Call setDetails() method of the object to set the input values.

10.Call display() method of the object to show the student details.

11.End the program.





## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber: 212223220055
*/
import java.util.Scanner;
class prog{
    String name;
    int rollno;
    void setDetails(String name,int rollno){
        this.name=name;
        this.rollno=rollno;
    }
    void display(){
        System.out.println("Name: "+name);
        System.out.println("Roll Number: "+rollno);
    }
public static void main(String[]args){
        Scanner scan = new Scanner(System.in);
        String name= scan.next();
        int rollno = scan.nextInt();
        prog s = new prog();
        s.setDetails(name,rollno);
        s.display();
    }

}
```


## OUTPUT:

<img width="1226" height="413" alt="Screenshot 2025-11-19 105431" src="https://github.com/user-attachments/assets/41675db6-adf9-4229-bdd6-ed05303ff4a5" />


## RESULT:

Thus, the program creates a Student class in Java with variables name and rollNumber, define a method setDetails to assign values to these variables, and display them.



