# Higher-or-Lower-with-java
a small game of higher or lower just the code

the cod for the game:-

import java.util.Random;
import java.util.Scanner;

public class Main{
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        Random rand = new Random();

        int theNumber = rand.nextInt(10)+1;
        int attempts  = 0;

        System.out.println("enter the number between 1 and 10");
        System.out.println("you have 3 attempts");

        while(true){
            System.out.print("enter your guess: ");
            int guess = input.nextInt();
            attempts++;


            if(guess > 10){
                System.out.println("out of range!!");
                attempts = 0;
            }
            if(attempts == 3){
                System.out.println("you lost!!");
                break;
            }
            if(guess < 11){
                if(guess == theNumber){
                    System.out.println("You guessed!");
                    System.out.println("You found the number in " + attempts + " attempts.");
                    break;
                }
                else if(guess < theNumber){
                    System.out.println("to low!!");
                }
                else if(guess > theNumber){
                    System.out.println("to high!!");
                }
            }
        }
        input.close();
    }
}
