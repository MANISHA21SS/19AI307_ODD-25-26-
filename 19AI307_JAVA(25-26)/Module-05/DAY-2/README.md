# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:

<img width="909" height="322" alt="Screenshot 2025-11-25 150309" src="https://github.com/user-attachments/assets/a5172638-91e0-4e6e-83c0-ef9f349e111e" />


## AIM:

To write a Java program that serializes a collection of Student objects (e.g., ArrayList<Student>) into a file and then deserializes them back, displaying the stored student details. 

## ALGORITHM :

1.Start

2.Create a Student class that implements Serializable with fields:

int id

String name

double marks

Override toString() for easy display

3.Create a collection, e.g., ArrayList<Student> to store student objects.

Read input from the user:

Number of students n

For each student, read id, name, marks and create a Student object

Add each Student object to the ArrayList

4.Serialization:

Create a FileOutputStream for file students.dat

Wrap it in an ObjectOutputStream

Write the ArrayList<Student> object to the file using writeObject()

Close streams

5.Print confirmation: "Students serialized successfully into: students.dat"

6.Deserialization:

Create a FileInputStream for file students.dat

Wrap it in an ObjectInputStream

Read the object back using readObject() and cast it to ArrayList<Student>

Close streams

7.Print confirmation: "Students deserialized successfully from: students.dat"

8.Display the deserialized students

9.End




## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber:  212223220055
*/

import java.io.*;
import java.util.*;

class Student implements Serializable {
    private static final long serialVersionUID = 1L;
    int id;
    String name;
    double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class SerializeStudents {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = sc.nextInt();
        for (int i = 0; i < n; i++) {
            int id = sc.nextInt();
            sc.nextLine();
            String name = sc.nextLine();
            double marks = sc.nextDouble();
            if (i < n - 1) sc.nextLine();
            students.add(new Student(id, name, marks));
        }

        String filename = "students.dat";

        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(filename))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + filename);
        } catch (IOException e) {
            System.out.println("Serialization Error: " + e.getMessage());
        }

        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(filename))) {
            Object obj = ois.readObject();
            if (obj instanceof List<?>) {
                List<?> tempList = (List<?>) obj;
                List<Student> deserializedStudents = new ArrayList<>();
                for (Object o : tempList) {
                    if (o instanceof Student) {
                        deserializedStudents.add((Student) o);
                    }
                }
                System.out.println("Students deserialized successfully from: " + filename);
                System.out.println();
                System.out.println("Deserialized Students:");
                for (Student s : deserializedStudents) {
                    System.out.println(s);
                }
            }
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Deserialization Error: " + e.getMessage());
        }

        sc.close();
    }
}

```

## OUTPUT:

<img width="1184" height="813" alt="Screenshot 2025-11-25 150630" src="https://github.com/user-attachments/assets/b0fe087f-6bed-46dd-9382-1b50453cdffd" />


## RESULT:

Thus the program has executed successfully to write a Java program that serializes a collection of Student objects  into a file and then deserializes them back, displaying the stored student details.
