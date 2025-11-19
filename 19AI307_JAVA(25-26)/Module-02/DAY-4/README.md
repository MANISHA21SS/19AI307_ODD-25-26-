# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:

<img width="1069" height="243" alt="Screenshot 2025-11-19 104844" src="https://github.com/user-attachments/assets/adf05297-6290-4917-a71e-ced17327a046" />

## AIM:

To create a Student class in Java with private instance variables for student ID, name, and age, initialize them using a constructor, and display the student details.

## ALGORITHM :

1.Start the program.

2.Import java.util.Scanner for input.

3.Create a class Student.

4.Declare private instance variables: studentID, studentName, and studentAge.

5.Define a constructor that accepts parameters for ID, name, and age and initializes the instance variables.

6.Create a method displayDetails() to print the student information.

7.Create a Main class with the main method.

8.Take input from the user for student ID, name, and age using Scanner.

9.Create an object of the Student class, passing the input values to the constructor.

10.Call the displayDetails() method of the object to show the student details.

11.End the program.





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber: 212223220055 
*/
import java.util.Scanner;
class Student{
    private int id;
    private String name;
    private int age;
    public Student(int id, String name, int age){
        this.id=id;
        this.name=name;
        this.age=age;
    }
        public void displayDetails(){
            System.out.println("Student Details:");
            System.out.println("Student ID: "+id);
            System.out.println("Student Name: "+name);
            System.out.println("Student Age: "+age);
        }
    }
    public class Main{
        public static void main(String[]args){
            Scanner scan = new Scanner(System.in);
            int id=scan.nextInt();
            String name = scan.next();
            int age = scan.nextInt();
            Student s = new Student(id,name,age);
            s.displayDetails();
        }
    }

```



## OUTPUT:

<img width="1233" height="558" alt="Screenshot 2025-11-19 105111" src="https://github.com/user-attachments/assets/1d5eef63-fa43-47b5-8ee2-55b3c1735b6e" />


## RESULT:

Thus, the program creates a Student class in Java with private instance variables for student ID, name, and age, initialize them using a constructor, and display the student details.

