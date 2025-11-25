# Ex.No:5(C)  FILE HANDLING USING JAVA

## QUESTION:

<img width="837" height="372" alt="Screenshot 2025-11-25 150815" src="https://github.com/user-attachments/assets/3f33f8ac-bbb4-434a-9a24-918fbd5a3211" />


## AIM:

To write a Java program that reads a text file line by line and reverses the order of words in each line, then displays the reversed lines. 

## ALGORITHM :

1.Start

2.Open the file for reading using BufferedReader wrapped around FileReader.

3.Read each line of the file using readLine() in a loop.

4.For each line:

Split the line into words using split("\\s+").

Reverse the order of the words.

Join the reversed words back into a single string.

Print the reversed line.

5.Repeat step 3–4 until the end of the file.

6.Close the BufferedReader.

7.End





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber: 212223220055
*/

import java.io.*;
import java.util.*;

public class ReverseWordsInLines {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        List<String> lines = new ArrayList<>();

        while (sc.hasNextLine()) {
            String line = sc.nextLine();
            if (line.equalsIgnoreCase("exit")) {
                break;
            }
            lines.add(line);
        }

        System.out.println("Reversed lines:");
        for (String line : lines) {
            String[] words = line.trim().split("\\s+");
            StringBuilder reversed = new StringBuilder();
            for (int i = words.length - 1; i >= 0; i--) {
                reversed.append(words[i]);
                if (i > 0) reversed.append(" ");
            }
            System.out.println(reversed.toString());
        }

        sc.close();
    }
}

```

## OUTPUT:

<img width="981" height="336" alt="Screenshot 2025-11-25 151048" src="https://github.com/user-attachments/assets/58ccbe3d-5ac7-4c90-a25d-b7918942e562" />


## RESULT:
Thus the program has executed successfully to write a Java program that reads a text file line by line and reverses the order of words in each line, then displays the reversed lines. 

