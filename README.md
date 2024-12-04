# TASK1

#Random number 
 
import java.util.Random; 
 
public class RandomNumberGenerator { 
    public static void main(String[] args) { 
        Random random = new Random(); 
        int randomNumber = random.nextInt(100) + 1; 
        System.out.println("Random number between 1 and 100: " + randomNumber); 
    } 
} 
2). Prompt the user 
import java.util.Random; 
import java.util.Scanner; 
 
public class RandomNumberGuessingGame { 
    public static void main(String[] args) { 
        Random random = new Random(); 
        int randomNumber = random.nextInt(100) + 1; 
 
        Scanner scanner = new Scanner(System.in); 
        System.out.print("Guess the random number between 1 and 100: "); 
        int userGuess = scanner.nextInt(); 
 
        if (userGuess == randomNumber) { 
            System.out.println("Congratulations! You guessed the correct number: " + randomNumber); 
        } else { 
            System.out.println("Sorry, the correct number was " + randomNumber + ". Your guess was: " + 
userGuess); 
        } 
    } 
} 
import java.util.Random; 
import java.util.Scanner; 
 
public class RandomNumberGuessingGame { 
    public static void main(String[] args) { 
        Random random = new Random(); 
        int randomNumber = random.nextInt(100) + 1; 
 
        Scanner scanner = new Scanner(System.in); 
        int userGuess = 0; 
 
        while (userGuess != randomNumber) { 
            System.out.print("Guess the random number between 1 and 100: "); 
            userGuess = scanner.nextInt(); 
 
            if (userGuess < randomNumber) { 
                System.out.println("Too low! Try again."); 
            } else if (userGuess > randomNumber) { 
                System.out.println("Too high! Try again."); 
            } 
        } 
 
        System.out.println("Congratulations! You guessed the correct number: " + randomNumber); 
    } 
} 
 
5) 
import java.util.Random; 
import java.util.Scanner; 
 
public class RandomNumberGuessingGame { 
    public static void main(String[] args) { 
        Random random = new Random(); 
        int randomNumber = random.nextInt(100) + 1; 
         
        Scanner scanner = new Scanner(System.in); 
        int userGuess = 0; 
        int maxAttempts = 5; 
        int attempts = 0; 
 
        System.out.println("You have " + maxAttempts + " attempts to guess the correct number 
between 1 and 100."); 
 
        while (attempts < maxAttempts) { 
            System.out.print("Attempt " + (attempts + 1) + ": Guess the random number: "); 
            userGuess = scanner.nextInt(); 
            attempts++; 
 
            if (userGuess == randomNumber) { 
                System.out.println("Congratulations! You guessed the correct number: " + randomNumber); 
                break; 
            } else if (userGuess < randomNumber) { 
                System.out.println("Too low! Try again."); 
            } else { 
                System.out.println("Too high! Try again."); 
            } 
 
            if (attempts == maxAttempts) { 
                System.out.println("Sorry, you've used all your attempts. The correct number was: " + 
randomNumber); 
            } 
        } 
    } 
} 
