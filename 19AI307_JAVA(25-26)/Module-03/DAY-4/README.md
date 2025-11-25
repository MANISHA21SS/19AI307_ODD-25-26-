# Ex.No:3(D)    INTERFACE 

## QUESTION:

<img width="1097" height="596" alt="Screenshot 2025-11-25 113859" src="https://github.com/user-attachments/assets/efd1175a-b874-4fcc-8124-349499797025" />


## AIM:

To write a Java program using inheritance and method overriding where different judges determine the result of a fight based on distinct scoring criteria. The program should output WIN, LOSE, or DRAW according to the judge selected.

## ALGORITHM :

1.Start the program.

2.Read inputs:

player1Score

player2Score

judgeType (1 = LenientJudge, 2 = StrictJudge)

3.Create a base class Judge with a method:

String decideResult(int diff) → returns result (default implementation may be empty or abstract)

4.Create a subclass LenientJudge:

If score difference ≥ 5 → WIN

If difference < 5 → DRAW

If player1Score < player2Score → LOSE

5.Create a subclass StrictJudge:

If difference ≥ 10 → WIN

If difference < 10 → DRAW

If player1Score < player2Score → LOSE

6.In main():

Compute diff = player1Score - player2Score

Based on judgeType:

7.Create corresponding judge object

Call decideResult(diff)

Print the result.

8.End the program.



## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber: 212223220055  
*/

import java.util.*;

interface FightJudge {
    String decideResult(int p1, int p2);
}

class LenientJudge implements FightJudge {
    public String decideResult(int p1, int p2) {
        int diff = p1 - p2;
        if (Math.abs(diff) >= 5) {
            return diff > 0 ? "WIN" : "LOSE";
        }
        return "DRAW";
    }
}

class StrictJudge implements FightJudge {
    public String decideResult(int p1, int p2) {
        int diff = p1 - p2;
        if (Math.abs(diff) >= 10) {
            return diff > 0 ? "WIN" : "LOSE";
        }
        return "DRAW";
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int player1 = sc.nextInt();
        int player2 = sc.nextInt();
        int judgeType = sc.nextInt();

        FightJudge judge;

        if (judgeType == 1)
            judge = new LenientJudge();
        else
            judge = new StrictJudge();

        System.out.println(judge.decideResult(player1, player2));
    }
}


```


## OUTPUT:

<img width="1119" height="295" alt="Screenshot 2025-11-25 114154" src="https://github.com/user-attachments/assets/5068ed15-5393-4180-a701-28e3aad7abc6" />


## RESULT:
Thus the program has executed successfully to write a Java program using inheritance and method overriding where different judges determine the result of a fight based on distinct scoring criteria.
