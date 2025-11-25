# Ex.No:3(C) ABSTRACTION

## QUESTION:

<img width="1182" height="558" alt="Screenshot 2025-11-25 113347" src="https://github.com/user-attachments/assets/82419504-b34d-4172-8679-e8ca42a9a002" />


## AIM:

To write a Java program using abstract classes to calculate the final score of different game types. The program should use an abstract class GameScore with an abstract method finalScore(), and subclasses should implement their own score formulas.

## ALGORITHM :

1.Start the program.

2.Create an abstract class GameScore containing:

An abstract method int finalScore().

3.Create a subclass ArcadeGame that:

Takes baseScore and level.

Calculates final score = baseScore + (level × 100).

4.Create another subclass PuzzleGame that:

Takes attempts.

If attempts ≤ 3 → score = 1000 − (attempts × 100)

Else → score = 500

5.In main():

Read the first input → game type (1 = Arcade, 2 = Puzzle).

If input is 1:

Read baseScore and level.

Create ArcadeGame object and print finalScore().

If input is 2:

Read attempts.

Create PuzzleGame object and print finalScore().

6.End program.





## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber: 212223220055 
*/

import java.util.Scanner;
abstract class GameScore{
      abstract int finalScore();
}
class ArcadeGame extends GameScore{
    int baseScore;
    int level;
    ArcadeGame(int baseScore,int level){
        this.baseScore=baseScore;
        this.level=level;
    }
    int finalScore(){
        return baseScore + (level * 100);
}
}
class PuzzleGame extends GameScore{
    int attempts;
    PuzzleGame(int attempts){
        this.attempts=attempts;
    }
    int finalScore(){
          if(attempts<=3)
               return 1000 - (attempts*100);
          else
                return 500;
   }
}
public class Main{
     public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        int choice = sc.nextInt();
        if(choice ==1){
            int base = sc.nextInt();
            int level =sc.nextInt();
            ArcadeGame ag = new ArcadeGame(base,level);
            System.out.println(ag.finalScore());
        }else if(choice==2){
            int attempts=sc.nextInt();
            PuzzleGame puzz = new PuzzleGame(attempts);
            System.out.println(puzz.finalScore());
       }else{
             System.out.println("Invalid choice");
      }
    }
}

```


## OUTPUT:

<img width="1085" height="206" alt="Screenshot 2025-11-25 113720" src="https://github.com/user-attachments/assets/ee02966d-c468-4ac9-8772-731d7ab836ea" />



## RESULT:
Thus the program has executed successfully to write a Java program using abstract classes to calculate the final score of different game types.
