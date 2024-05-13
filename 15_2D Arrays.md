### ONE DIMENSIONAL ARRAY

![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/58497c2a-0884-4920-b796-479d625106df)

```java
public class Main {
  public static void main(String[] args) {
    int[] oneDimensionalArray = {1, 2, 3};

    for(int i = 0; i < oneDimensionalArray.length; i++){
        System.out.print(oneDimensionalArray[i]);
     }
   }
}
```

### TWO DIMENSIONAL ARRAY

![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/e9fe110d-8229-4589-be97-c1179cedea2f)

```java
public class Main {
    public static void main(String[] args) {
        int[][] array = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        for(int i = 0; i < array.length; i++){ 
            //array[0] = {1, 2, 3}
            //array[0].length = 3
            int[] row = array[i]; // {1, 2, 3} OR {4, 5, 6}...
            for(int j = 0; j < row.length; j++){  //PROCESSING ROWS HERE
                System.out.print(row[j]); 
            }
        }  
    }
}
```

![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/e68918c4-709b-4a54-bcc5-48cb0e24326d)

```java
public class Main {
    public static void main(String[] args) {
        int[][] array = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };
        for(int i = 0; i < array.length; i++){ 
        
            int[] row = array[i]; // {1, 2, 3} OR {4, 5, 6} ...
            for(int j = 0; j < row.length; j++){
                System.out.print(row[j]); 
            }
            
            System.out.print("|");
        }  
    }
}
```

![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/3bd06b7a-21eb-4f2c-af75-f2b0853c75c9)

```java
public class Main {
    public static void main(String[] args) {
        int[][] array = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };
        for(int i = 0; i < array.length; i++){ 
        
            int[] row = array[i]; // {1, 2, 3} OR {4, 5, 6} ...
            for(int j = 0; j < row.length; j++){
                System.out.print(row[j]); 
            }
            
            System.out.println();
        }  
    }
}
```
https://replit.com/@gracenaja/15Java2DArraySimple09052024#src/main/java/Main.java

## Game Board

![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/abca9107-2062-4f9a-8e01-6a351b72a1a5)


```java
public class Main{
  public static void main (String[] args) {

    int[][] arr = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };   

    System.out.println("Game Board: \n");

    for(int i = 0; i < arr.length; i++){
      for(int j = 0; j < arr.length; j++){
        System.out.print(" " + arr[i][j] + " |");
      }
    System.out.println();
    System.out.println("------------");
    }
  }
}
```
https://replit.com/@gracenaja/15JavaGame-Board-Tick-Tack-Toe#src/main/java/Main.java


![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/92a16f29-45cd-4e74-88e4-016f9b643ea0)

```java
public class Main {
    public static void main(String[] args) {
        int[][] array = new int[5][5];

        for (int i = 0; i < array.length; i++) {
            int[] row = array[i];
            for (int j = 0; j < row.length; j++) {
                row[j] = i;
            }
        }
        for(int i = 0; i < array.length; i++){
            for(int j = 0; j < array[i].length; j++){
                System.out.print(array[i][j] + "|");
            }
            System.out.println();
            System.out.println("----------");
        }
    }
}
```
![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/b370c8f4-82a8-4a28-8276-e618202f0942)
![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/8f79a87d-b3a4-4930-a359-5554598718bd)
![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/fe7f9fa6-9e76-4287-a665-ffa1f22c0ee4)

```java
public class Main {
    public static void main(String[] args) {
        int[][] array = new int[5][5];

        for (int i = 0; i < array.length; i++) {
            int[] row = array[i];
            for (int j = 0; j < row.length; j++) {
                row[j] = i;  // = j    // = 1
            }
        }
        for(int i = 0; i < array.length; i++){
            for(int j = 0; j < array[i].length; j++){
                System.out.print(array[i][j] + "|");
            }
            System.out.println();
            System.out.println("----------");
        }
    }
}```
https://replit.com/@gracenaja/15Java2DArrays#src/main/java/Main.java









## Fill the 5x5 array with numbers from 1 to 25

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
}
```

https://replit.com/@gracenaja/15Java2DArrayHW1-to-25#src/main/java/Main.java

## Fill the array with random digits from 0 to 9

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
}
```

https://replit.com/@gracenaja/15JavaRandom-Nr-Table#src/main/java/Main.java




