# Ex.No:3(b) POLYMORPHISM

## QUESTION:

<img width="1258" height="584" alt="Screenshot 2025-11-25 112643" src="https://github.com/user-attachments/assets/ff3bcb28-f88f-46d5-a508-01fea6ffc8d4" />


## AIM:
To write a Java program that simulates a hotel booking system using method overloading, where one method handles single-day bookings and another overloaded method handles multi-day bookings based on user input.

## ALGORITHM :

1.Start the program.

2.Create a class HotelBooking.

3.Define a method bookRoom(String roomType):

Display per-night charge based on room type.

4.Define an overloaded method bookRoom(String roomType, int nights):

Multiply per-night rate by number of nights.

5.Display total charge.

6.In the main() method:

Ask the user to enter room type.

Ask whether the booking is for multiple nights.

If no, call bookRoom(roomType).

If yes, ask for number of nights and call bookRoom(roomType, nights).

7.Print booking confirmation.

8.End program.




## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber: 212223220055 
*/

import java.util.Scanner;

class HotelBooking {

    // Overloaded method for single-day booking
    public void bookRoom(String roomType) {
        int rate = getRate(roomType);
        System.out.println(roomType + "   booked. ₹" + rate + " per night.");
    }

    // Overloaded method for multi-day booking
    public void bookRoom(String roomType, int nights) {
        int rate = getRate(roomType);
        int total = rate * nights;
        System.out.println(roomType + "   booked for " + nights + " nights. Total: ₹" + total);
    }

    // Helper method to determine rate per room type
    private int getRate(String roomType) {
        switch (roomType.toLowerCase()) {
            case "single room":
                return 1000;
            case "double room":
                return 1000;
            case "suite":
                return 1000;
            default:
                return 1000; // default rate
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        HotelBooking hotel = new HotelBooking();
        String roomType = sc.nextLine().trim();
        String choice = sc.nextLine().trim().toLowerCase();

        if (choice.equals("yes")) {
            int nights = sc.nextInt();
            hotel.bookRoom(roomType, nights); // multi-day booking
        } else {
            hotel.bookRoom(roomType); // single-day booking
        }

        sc.close();
    }
}

```


## OUTPUT:

<img width="1221" height="334" alt="Screenshot 2025-11-25 113156" src="https://github.com/user-attachments/assets/6df5c093-3869-4ec0-8070-f1ec10ce1a02" />


## RESULT:
Thus the program has executed successfully to write a Java program that simulates a hotel booking system using method overloading, where one method handles single-day bookings and another overloaded method handles multi-day bookings based on user input.

