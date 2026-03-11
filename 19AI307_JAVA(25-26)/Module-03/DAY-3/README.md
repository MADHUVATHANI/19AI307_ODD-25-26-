# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create abstract class GameScore with method finalScore().
Subclasses:
ArcadeGame: score = baseScore + (level × 100)
PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500

## AIM:

To Create abstract class GameScore with method finalScore().

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Based on the game type, create the corresponding object:ArcadeGame then read base score and level ,PuzzleGame then read number of attempts.
4.	Through runtime polymorphism, call the overridden method finalScore() of the respective game class.
5.	Compute the score based on game rules:ArcadeGame: baseScore + (level × 100)
6.	PuzzleGame: if attempts ≤ 3 → 1000 − attempts × 100; else → 500
7.	Print the final score and stop.





## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.*;

abstract class GameScore {
    abstract int finalScore();
}

class ArcadeGame extends GameScore {
    private int baseScore;
    private int level;

    public ArcadeGame(int baseScore, int level) {
        this.baseScore = baseScore;
        this.level = level;
    }

    @Override
    int finalScore() {
        return baseScore + (level * 100);
    }
}

class PuzzleGame extends GameScore {
    private int attempts;

    public PuzzleGame(int attempts) {
        this.attempts = attempts;
    }

    @Override
    int finalScore() {
        if (attempts <= 3) {
            return 1000 - (attempts * 100);
        } else {
            return 500;
        }
    }
}

public class GameScoreCalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int gameType = sc.nextInt(); 
        
        GameScore game;
        if (gameType == 1) {
            int base = sc.nextInt();
            int level = sc.nextInt();
            game = new ArcadeGame(base, level);
        } else if (gameType == 2) {
            int attempts = sc.nextInt();
            game = new PuzzleGame(attempts);
        } else {
            System.out.println("Invalid game type!");
            sc.close();
            return;
        }
        
        System.out.println(game.finalScore());
        sc.close();
    }
}
```






## OUTPUT:

<img width="452" height="316" alt="image" src="https://github.com/user-attachments/assets/d8e30677-32f8-4a37-88de-766429b19c4d" />


## RESULT:

Thus, the program to create abstract class GameScore with method finalScore() executed successfully.


