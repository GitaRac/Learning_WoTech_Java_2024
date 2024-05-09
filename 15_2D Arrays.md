Fill the 5x5 array with numbers from 1 to 25
![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/206ecc23-f3e3-4023-a570-1cc0393874ca)
```java
public class Main {
    public static void main(String[] args) {
        int[][] array = new int[5][5];
        int counter = 1; //start from 1

        // Fill with numbers  1 - 25
        for (int i = 0; i < array.length; i++) {
            for (int j = 0; j < array[i].length; j++) {
                array[i][j] = counter;
                counter++;
            }
        }
        // Printout
        for (int i = 0; i < array.length; i++) {
            for (int j = 0; j < array[i].length; j++) {
                if (array[i][j] < 10) {
                    System.out.print(" " + array[i][j] + "  "); // 1+2 spaces for 1-9
                } else {
                    System.out.print(array[i][j] + "  "); // 2 spaces for 10-25
                }
            }
            System.out.println(); // Move to the next line after printing each row
        }
    }
}```
https://replit.com/@gracenaja/15Java2DArrayHW1-to-25#src/main/java/Main.java

Fill the array with random digits from 0 to 9
![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/91408e1f-e3e5-4b69-8711-0f8441b9b494)
```java
import java.util.Random;

public class Main {
    public static void main(String[] args) {
        int[][] array = new int[5][5];
        Random random = new Random();

        // Fill the array with random digits 0 - 9
        for (int i = 0; i < array.length; i++) {
            for (int j = 0; j < array[i].length; j++) {
                array[i][j] = random.nextInt(10); // random 0 and 9
            }
        }

        // Printout
        for (int i = 0; i < array.length; i++) {
            for (int j = 0; j < array[i].length; j++) {
                System.out.print(array[i][j] + "  "); // each element with two spaces
            }
            System.out.println(); // Move to the next line after printing each row
        }
    }
}```
https://replit.com/@gracenaja/15JavaRandom-Nr-Table#src/main/java/Main.java




