# 180424
##110424 fizbuzz
```java
import java.util.Scanner;
public class Main {
  public static void main(String[] args) {
  Scanner scanner = new Scanner(System.in);
  System.out.println("Insert a number");

  int number =  scanner.nextInt();
    
  for (int i = 1; i <= number; i++) {
    
    String result = "";
 
    if (i % 3 == 0) {
      result += "Wo";
  }  
    if (i % 5 == 0) {
    result += "Tech";
  } 
    if(result.equals("")){ //if result empty
      result = String.valueOf(i); // result = i
    }
    System.out.println(result);

    scanner.close();
    }
  }
}


/* Team work: Develop a program, that iterates through numbers from 0 till X amount of times (X is user provided)
For numbers that are divided by 3: print out "Wo" .

For numbers that are divided by 5: print out "Tech". 

For numbers divided by 3 and 5: print out "WoTech". */
```

## 180424
 
```java
// Fill the party list wtih people you would like to invite to the party. Check whether or not ann and maris are in the array

import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    String[] partyList = {"Oskars", "Anna", "Andris", "Johanna", "Marta"};
    
  Scanner scanner = new Scanner(System.in);
  
  System.out.println("What name would you like to check from the invitation list?");
    
  String input = scanner.nextLine().toLowerCase();
    
  boolean isInvited = false;
  for(String name : partyList){
   if(name.toLowerCase().equals(input)){
     isInvited = true;
     break;
   }
  }
    if (isInvited){
  System.out.println(input + " is in the party list");
   } else {
    System.out.println(input + " is not in the party list");
}
    scanner.close();
  }
    
}
```

```java
/* Give an array of integers, write a Java program to find the maximum sum of two integers in the array eg [1,2,3,4,5] the max sum would be 4+5 */


public class Main {
  public static void main(String[] args) {

    
  int[] array = {10, 20, 60, 40, 30};

   
    int maxSum = Integer.MIN_VALUE;
    int num1 = 0;
    int num2 = 0;
    
    for(int i = 0; i < array.length; i++){
        for(int j = i + 1; j < array.length; j++){
            if(array[i] + array[j] > maxSum){
             num1 = array[i];
             num2 = array[j];
            maxSum = num1 + num2;
      }
      }
      }
    
      
    System.out.println("The maximum sum is " + maxSum); 
    System.out.println("The two numbers are " + num1 + " and " + num2);
  }
  }
  
```
