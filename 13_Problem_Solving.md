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

        // Convert StringBuilder back to a String
        String reversedWord = reverse.toString();

        // Check if the lowercase word is equal to its reversed version
        return lowercaseWord.equals(reversedWord);
    }
}
```


