```java
/* Develop a simple book management application with ArrayList.
User should be able to add a book to ArrayList. +
User should be able to remove a book from ArrayList.
Easy: Work with String in ArrayList. All the actions should be available for user.
Medium: Work with String User should be able to repeat all the actions infinitely.
Hard: Create a Book class and work with Book object to the ArrayList.
*/
import java.util.Scanner;
public class Main {
  public static Library library = new Library();
  public static void main(String[] args) {
     Scanner scanner = new Scanner(System.in);
    handleUserActions();
     scanner.close();
  }
  public static void handleUserActions(){
    while(true){
      

    System.out.println("What do you want to do? (add | remove | view | quit)");
    String choice = scanner.nextLine();
      
      if (choice.equals("add")) {
        addBook();
        }
        
       
        
      } else if (choice.equals("remove")) {
        System.out.println("Enter the book title you want to remove: ");
        String title = scanner.nextLine();
        library.removeBook(title);
      } else if (choice.equals("view")) {
        library.viewBooks();
      } else if (choice.equals("quit")) {
        break; 
      } else {
        System.out.println("Invalid choice.");      
      }
      }

     
  }
   public static void addBook(){
     System.out.println("Enter the book title:");
       String title = scanner.nextLine();
       System.out.println("Enter the author:");
       String author = scanner.nextLine();
       System.out.println("Enter the year:");
       int year;
       while (true) {
           try {
               year = Integer.parseInt(scanner.nextLine());
               break;  
           } catch (NumberFormatException e) {
               System.out.println("Invalid year. Please enter a valid year:");
           }
       }
     Book book = new Book(title, year, author);
     library.addBook(book);
   }
    public static void removeBook(){
      System.out.println("Enter the title of the book you want to remove: ");
      String title = scanner.nextLine();
      library.removeBook(title);
    }
    public static void viewBooks(){
      library.viewBooks();
    }
    
    }
    

public class Book{
  public String title;
  public int year;
  public String author;
 
  
  public Book(String title, int year, String author) {
    this.title = title;
    this.year = year;
    this.author = author;
  }
}

import java.util.ArrayList;

public class Library{
  private ArrayList<Book> books = new ArrayList<Book>();

  public void addBook(Book book){
    books.add(book);
  }
  public ArrayList<Book> getBooks(){
    return books;
  }
  public void removeBook(String title) {
    for (int i = 0; i < books.size(); i++){
      if (books.get(i).title.equalsIgnoreCase(title)){
        books.remove(i);
        System.out.println("Book " + title + " removed successfully");
        return;
      }
    }
    System.out.println("Book " + title + " not found");
  }
  public void viewBooks(){
    if(books.isEmpty()){
      System.out.println("No books in the library");
    } else{
      for(Book book : book) {
        System.out.println(book.title + " by " + book.author + "(" + book.year + ")");
      }
    }
  }
}
```
