# 180424
##110424 fizbuzz
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
