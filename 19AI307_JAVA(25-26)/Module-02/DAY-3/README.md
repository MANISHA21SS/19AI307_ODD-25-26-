# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:

<img width="1163" height="803" alt="Screenshot 2025-11-19 104528" src="https://github.com/user-attachments/assets/0f40e882-c120-4567-bd9a-77c4c08dcd2d" />

## AIM:

To create a Java class Rectangle with private instance variables length and width, and allow modification and access through public getter and setter methods, and calculate the area.

## ALGORITHM :

1.Start

2.Define a class Rectangle with:

Private variables: length, width

Public setters setLength(), setWidth()

Public getters getLength(), getWidth()

Method calculateArea() that returns length * width

3.In main:

Create a Rectangle object.

Read length and width from user.

Set these values using setter methods.

Call calculateArea() to get the area.

4.Print the result.

5.Stop





## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber: 212223220055
*/
import java.util.Scanner;
class Rectangle{
    private double length;
    private double width;
    public double getLength(){
        return length;
    }
    public void setLength(double length){
        this.length=length;
    }
    public double getWidth(){
        return width;
    }
    public void setWidth(double width){
        this.width=width;
    }
    public double calculateArea(){
        return length*width;
    }
}
public class Main{
    public static void main(String[]args){
        Scanner scan = new Scanner(System.in);
        Rectangle rect = new Rectangle();
        double length = scan.nextDouble();
        rect.setLength(length);
        double width = scan.nextDouble();
        rect.setWidth(width);
        System.out.println("Length: "+rect.getLength());
        System.out.println("Width: "+rect.getWidth());
    }
}
```


## OUTPUT:

<img width="1227" height="466" alt="Screenshot 2025-11-19 104637" src="https://github.com/user-attachments/assets/e19a3e28-f903-4093-ad45-a5d0dd59250e" />


## RESULT:

Thus, the program creates a Java class Rectangle with private instance variables length and width, and allow modification and access through public getter and setter methods, and calculate the area.
