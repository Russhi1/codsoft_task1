# Task 1


## Number Game in Java

### Overview

* The game generates random numbers from 1 to 100(using Random class) and We have to guess the correct number
* We get 5 chances in total
* If the guessed number is higher the code prints that the humber is high and prompts us to try again
* If the guessed number is lower the code prints that the humber is low and prompts us to try again
* The code also tracks the number of times You have won the game

# Code

```
import java.util.Random;
import java.util.Scanner;

public class Random1 {
    public static void main(String [] args){
        //Random number object
        boolean playagain = true;
        Scanner sc = new Scanner(System.in);
        System.out.println("");
        System.out.println("Welcome to the Number Guessing game");
        System.out.println("Guess any number from 1 to 100");

        //Enter you guess
        while(playagain){
            int attemptsused = 0;
            Random ran1 = new Random();
            int x = ran1.nextInt(100) + 1;
            int maxattempts = 5;
            int roundswon = 0;
            System.out.println("Enter your guess number");


        //Checking the guessed number
             for(int i=0;i<maxattempts;i++){
                 int guess = sc.nextInt();
                 attemptsused++;


                 if(guess==x){
                     System.out.println("Congratulations!! You got it right");
                     System.out.println("You used" + " " + attemptsused + " " + "number of attempts");
                     roundswon++;
                     break;
                    }
                 else if(guess <x){
                     System.out.println("Low! Try again");
                    }
                 else{
                     System.out.println("High! try again");

                    }
                 if (i == maxattempts -1){
                     System.out.println("You have used all your attempts :(");
                     System.out.println("The correct number was:" + x);
                     }
                    }
                System.out.println("Would you like to play again? (Y/N)");
                sc.nextLine();
                String ans = sc.nextLine();
                playagain = ans.equalsIgnoreCase("Y");

                //Final Result of youyr performance

                if(ans.equalsIgnoreCase("N")){
                    System.out.println("Your Score :");
                    System.out.println("Number of rounds won:" + roundswon);
                    
                    
                }
                }
sc.close(); 
}

}


```

# Output

![Screenshot 2025-02-19 123229](https://github.com/user-attachments/assets/22b0075b-2adf-42db-b636-8ab8fb990129)


