![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/5d3026be-2c8f-4461-8560-cac68b635d7b)

https://replit.com/@gracenaja/12JavaTitle-borderdescription#src/main/java/Main.java

```java
/*
  Ask user for a title - inputText()
  Ask user for a description - inputText()

  PrintInformation()
    Figure out the size of title
    Print out a border of the size of the title -> printBorder()
    Print out the title
    Print out a border of the size of the title -> printBorder()
    Print out the description
*/
import java.util.Scanner;
public class Main {
  public static void main(String[] args) {

    //Creating scanner
    Scanner scanner = new Scanner(System.in);

    //Calling method for getting title
    System.out.print("Enter a title: ");
    String title = getText();

    System.out.print("Enter a description: ");
    String description = getText();

    //Calling method to get printout with lines
    getPrintout(title, description);

    //Closing scanner
    scanner.close();
  }

  // Method to ask user for input
  public static String getText() {
    Scanner scanner = new Scanner(System.in);

    //Read user input
    String text = scanner.nextLine();

    //Return user input
    return text;
  }

    // Method to display the result with the title wrapped in = characters + description

  public static void getPrintout(String title, String description) {

    // Calculate length
    int length = title.length();
    System.out.println("");
    // Create top border
    printBorder(length);
    // Display the title
    System.out.println(title);
    
    // Create bottom border
    printBorder(length);

    // Display the description
    System.out.println("");
    System.out.println(description);

  }

  public static void printBorder(int length){
    for (int i = 0; i < (length); i++) {
      System.out.print("=");
    }
    System.out.println("");
  }
}
```
![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/61f6dac3-3674-4917-9631-0e9c8f5c466c)
```java
public class Main {
  public static void main(String[] args) {

    int number = 51;

    if(number > 50){
      System.out.println("Number is greater than 50");
    }else if(number < 50){
      System.out.println("Number is less than 50");
    }else{
      System.out.println("Number is equal to 50");  
    }

    int number2 = 49;
    
    if(number2 > 50){
      System.out.println("Number is greater than 50");
    }else if(number2 < 50){
      System.out.println("Number is less than 50");
    }else{
      System.out.println("Number is equal to 50");  
    }
    
  }
}
```


![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/dc498068-90ec-40f3-b141-2703d1285b31)


```java
public class Main {
  public static void main(String[] args) {
    
    int money = 50;

    String result = buyJeans(money);

    System.out.println(result);
  }

  public static String buyJeans(int money){
    int price = 30;
    if(money > price) // 29.99
    {
      return "Person can afford Jeans";
    }else{
      return "Person cannot afford Jeans";
    }
  }
}
```
![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/f64e0b32-f053-4abf-a710-6a592e6cdbe7)

```java
// 7, 12, 18 
// Needs to sum them all together

public class Main {
  public static void main(String[] args) {
    int number1 = 7;
    int number2 = 12;

    int number3 = 18;

    int result = sum(number1, number2); // 7 + 12 = 19

    int finalResult = sum(result, number3); // 19 + 18 = 37

    System.out.println(finalResult);
  }

  public static int sum(int a, int b){
    return a + b;
  }
}
```

```java
// 7, 12, 18 
// Needs to sum them all together

public class Main {
  public static void main(String[] args) {
    int n1 = 7;
    int n2 = 12;
    int n3 = 18;

    int result = sum(n1, n2, n3);

    System.out.println(result);
  }

  public static int sum(int a, int b, int c) {
    return a + b + c;
  }
}
```

![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/9a60fad3-52be-417f-8c26-ef496f39a751)
```java
// function - return smallest number of 2 numbers

import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int[] numbers = new int[2]; 
        System.out.println("Enter the first number: ");
        numbers[0] = scanner.nextInt(); 
        System.out.println("Enter the other number: ");
        numbers[1] = scanner.nextInt(); 
        int smallest = findSmallest(numbers);
        System.out.println("The smallest number is: " + smallest);
    }
    public static int findSmallest(int[] numbers) {
        int smallest = numbers[0];
        for (int i = 1; i < numbers.length; i++) { 
            if (numbers[i] < smallest) {
                smallest = numbers[i];
            }
        }
        return smallest;
    }
}
```




