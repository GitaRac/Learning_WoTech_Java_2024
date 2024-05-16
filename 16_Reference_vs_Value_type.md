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


![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/a64825da-e541-46a7-b723-1f40408fcd1c)

```java
public class Main {
    public static void main(String[] args) { 
        int[] arrayVoid = { 1, 2, 3, 4, 5 }; 
        printOutArray(arrayVoid);
    }

    public static void printOutArray(int[] array) { 
        for (int i = 0; i < array.length; i++) {
            System.out.println(array[i]);
        }
    }
}
```


![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/cb83c067-8107-4629-86d7-a779c4b6ab43)

```java
public class Main {
    public static void main(String[] args) { 
        int[] arrayVoid = { 1, 2, 3, 4, 5 }; 

        int[] array = arrayVoid;
        array[0] = 100;

        printOutArray(arrayVoid);
    }

    public static void printOutArray(int[] array) { 
        for (int i = 0; i < array.length; i++) {
            System.out.println(array[i]);
        }
    }
}
```

![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/4ab5c54e-076b-4534-9b5b-5000da3b378a)

```java
public class Main {
    public static void main(String[] args) { 
        
        int[] arrayVoid = { 1, 2, 3, 4, 5 }; 
        
        int[] array2 = new int[5];
        array2[0] = 1;
        array2[1] = 2;
        array2[2] = 3;
        array2[3] = 4;
        array2[4] = 5;

        System.out.print(arrayVoid == array2);
        // It is comparing the references of the arrays, not the values.
    }
}
```

![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/93c7d061-acb1-4e1e-8d8a-49c29e508e73)

``java
public class Main {
    public static void main(String[] args) { 
        
        int[] arrayVoid = { 1, 2, 3, 4, 5 }; 
        int[] array2 = { 1, 2, 3, 4, 5 };
       
        System.out.print(arrayVoid == array2);
        // It is comparing the references of the arrays, not the values.
    }
}
```

![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/a4180f8a-56b5-47c3-8868-f4e71d7ca743)

```java
public class Main {
    public static void main(String[] args) { 
        
        int[] arrayVoid = { 1, 2, 3, 4, 5 }; 
        int[] array2 = arrayVoid;
       
        System.out.print(arrayVoid == array2);
        // It is comparing the references of the arrays, not the values.
    }
}
```

![image](https://github.com/GitaRac/Learning_WoTech_Java_2024/assets/165934633/f9e8888b-53cd-46b3-ad63-4908145e75ef)

```java
public class Main {
    public static void main(String[] args) { 
        
        int[] arrayVoid = { 1, 2, 3, 4, 5 }; 
        
        int[] array2 = arrayVoid; // !!!
        array2[0] = 123; // so both arrays will be changed to this value
       
        System.out.println(arrayVoid == array2);
        System.out.println(arrayVoid[0]);
        System.out.println(array2[0]);
    }
}
```














