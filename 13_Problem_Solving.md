### 13_Java_Problem solving

## MY POSITION IN A RACE 🤾🏽‍♂️ of throwing a rock
![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/84db2def-7bd0-4f94-bd26-57498dde5c1f)
```java
public class Main {
    public static void main(String[] args) {
        // Define the list of distances in the race
        int[] raceDistances = {50, 47, 44};

        // My throw distance
        int myDistance = 46;

        // Compare my distance with the race distances
        int myPosition = getMyPosition(raceDistances, myDistance);

        // Display the result
        System.out.println("I threw " + myDistance + " metres.");
        System.out.println("My position in the race: " + myPosition);
    }

    // Method to determine the position based on distances
    public static int getMyPosition(int[] distances, int myDistance) {
        int position = 1; // Assume initial position is 1 (first place)

        // Iterate over each distance in the race
        for (int distance : distances) {
            // Compare my distance with the current race distance
            if (myDistance < distance) {
                position++; // If my distance is less, increment position
            }
        }
        return position;
    }
}
```
https://replit.com/@gracenaja/13JavaMyPositionInARace#src/main/java/Main.java


## PRIME NUMBERS
![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/94bde932-bd94-4db9-bb26-e06b3e5edd9f)
```java
public class Main {
    public static void main(String[] args) {
        int number = 1; // Change this number to check for primality

        if (isPrime(number)) {
            System.out.println(number + " is a prime number.");
        } else {
            System.out.println(number + " is NOT a prime number.");
        }
    }

    // Method to check if a number is prime
    public static boolean isPrime(int number) {
        // Handle special cases
        if (number <= 1) {
            return false; // Numbers less than or equal to 1 are not prime
        }
        if (number <= 3) {
            return true; // 2 and 3 are prime numbers
        }
        if (number % 2 == 0 || number % 3 == 0) {
            return false; // Exclude even numbers and multiples of 3
        }

        // Check divisibility for numbers of the form 6k ± 1
        for (int i = 5; i * i <= number; i += 6) {
            if (number % i == 0 || number % (i + 2) == 0) {
                return false; // If divisible by i or i + 2, not prime
            }
        }

        return true; // If not divisible by any smaller numbers, it's prime
    }
}
```
https://replit.com/@gracenaja/13JavaPrime-Nr#src/main/java/Main.java


## PALINDROME
![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/f41fb883-1878-4efc-88e3-9d704ecb71b8)
```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("PALINDROME WORDS");
        System.out.println("Enter a word to check:");
        String word = scanner.nextLine();

        boolean isPalindrome = checkPalindrome(word);
        if (isPalindrome) {
            System.out.println("\n" + word + " is a palindrome");
        } else {
            System.out.println("\n" + word + " is not a palindrome");
        }
        scanner.close();
    }

    public static boolean checkPalindrome(String word) {
        // Convert the input word to lowercase (or uppercase) for case-insensitive comparison
        String lowercaseWord = word.toLowerCase();

        // Create a StringBuilder to store the reversed version of the lowercase word
        StringBuilder reverse = new StringBuilder();
        for (int i = lowercaseWord.length() - 1; i >= 0; i--) {
            reverse.append(lowercaseWord.charAt(i));
        }

        // Convert StringBuilder back to a String to compare
        String reversedWord = reverse.toString();

        // Check if the lowercase word is equal to its reversed version
        return lowercaseWord.equals(reversedWord);
    }
}
```
https://replit.com/@gracenaja/13JavaPalindrome

## 21 STICKS GAME
![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/cc443bc5-979b-41db-8ae6-5db6e83fd3f4)
```JAVA
import java.util.Scanner;
public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int sticks = 21;
        System.out.println("🥖🥖🥖 Welcome to the 21 Sticks Game! 🥖🥖🥖");
        System.out.println("\nYou will pick first.");

        // Game loop
        while (true) {
            // Player's turn
            System.out.print("\nYour turn. Enter 1 or 2 to pick sticks: ");
            int playerPick = scanner.nextInt();

            // Validate player's input
            while (playerPick < 1 || playerPick > 2 || playerPick > sticks) {
                System.out.println("Invalid input. Please enter 1 or 2 (and not more than sticks left).");
                playerPick = scanner.nextInt();
            }

            sticks -= playerPick;
            System.out.println("Sticks left: " + sticks);

            // Check if player took the last stick
            if (sticks <= 0) {
                System.out.println("You took the last stick. Computer wins!");
                break;
            }

            // Computer's turn
            int computerPick = getComputerMove(sticks);
            System.out.println("Computer picks " + computerPick + " sticks.");
            sticks -= computerPick;
            System.out.println("Sticks left: " + sticks);

            // Check if computer took the last stick
            if (sticks <= 0) {
                System.out.println("Computer took the last stick. You win!");
                break;
            }
        }

        scanner.close();
    }

    // Method to determine computer's optimal move
    private static int getComputerMove(int sticksLeft) {
        // If there are 5 sticks left, take 1 to force a win
        if (sticksLeft == 5) {
            return 1;
        }
        // Otherwise, try to leave the player with 2 or 3 sticks
        // This is a winning strategy if played optimally
        else {
            int computerPick = (sticksLeft % 3 == 0) ? 2 : 1;
            return computerPick;
        }
    }
}
```
https://replit.com/@gracenaja/13Java21-Sticks-Game#src/main/java/Main.java

## HANGMAN




