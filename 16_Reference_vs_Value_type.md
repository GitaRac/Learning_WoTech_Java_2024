### Reference vs Value Type

![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/57a3463d-8805-41b5-81db-4bf0c5929573)

```java
// Reference vs value type
public class Main {
    public static void main(String[] args) {
        
        int number = 20; //changed
        number = changeNumber(number);
        System.out.println(number);

      
        int numberVoid = 30; // not changed
        changeNumberVoid(numberVoid);
        System.out.println(numberVoid);
    }
  

    public static int changeNumber(int number){
        number = 25;
        return number;
    }

    public static void changeNumberVoid(int number){
        number = 35; //THIS NUMBER WILL NOT CHANGE THE numberVoid value
    }
}
```

![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/07372454-8d4c-4dab-8d9b-d617f7183b09)

```java
public class Main {
      public static void main(String[] args) {
          int[] array = {1, 2, 3, 4, 5};
          array = changeArray(array);
          printOutArray(array);
      }

      public static int[] changeArray(int[] array){
          for(int i = 0; i < array.length; i++){
              array[i] = 0;
          }
          return array;
      }

      public static void printOutArray(int[] array){
          for(int i = 0; i < array.length; i++){
              System.out.println(array[i]);
          }
      }
  }
```

![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/7cb2b9eb-623f-482a-ba64-1865b5c13ecd)

```java
public class Main {
  public static void main(String[] args) { // Main method
      int[] array = { 1, 2, 3, 4, 5 }; // 1. declare an array
      array = changeArray(array); // 2. change the content of the array
      printOutArray(array); // 3. print out the values of the array

      int[] arrayVoid = { 1, 2, 3, 4, 5 }; // 4
      changeArrayVoid(arrayVoid); // 5
      printOutArray(arrayVoid); //6
  }

  public static int[] changeArray(int[] array) { // 2
      for (int i = 0; i < array.length; i++) { // 2.1.
          array[i] = 0; // 2.2
      } // 2.3
      return array; // 2.4
  }

  public static void changeArrayVoid(int[] array) { //5
      for (int i = 0; i < array.length; i++) { // 5.1
          array[i] = 1; // 5.2
      }// 5.3
  }

  public static void printOutArray(int[] array) { // 3 // 6
      for (int i = 0; i < array.length; i++) { // 3.1 //6.1
          System.out.println(array[i]);// 3.2 // 6.2
      } // 3.3 // 6.3
  }
}
```




