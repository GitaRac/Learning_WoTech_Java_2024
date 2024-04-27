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


