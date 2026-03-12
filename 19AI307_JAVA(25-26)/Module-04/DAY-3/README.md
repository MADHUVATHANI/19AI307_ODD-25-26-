# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:

Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).
## AIM:
To Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	For each book, read title and author and create a new Book object.
4.	Add each Book object to the Library’s internal list using composition.
5.	After all books are added, call showBooks() to display stored books.
6.	Print each book’s details (title and author) from the library.







## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.*;

public class CompositionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();
        sc.close();
    }
}

class Book {
    private String title;
    private String author;

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return title + " by " + author;
    }
}

class Library {
    private List<Book> books = new ArrayList<>();

    public void addBook(String title, String author) {
        books.add(new Book(title, author));
    }

    public void showBooks() {
        System.out.println("Books in Library:");
        for (Book b : books) {
            System.out.println("- " + b.getDetails());
        }
    }
}
```






## OUTPUT:

<img width="981" height="617" alt="image" src="https://github.com/user-attachments/assets/04652712-11e8-4a6c-ab93-35c73d0b287a" />


## RESULT:

Thus, the program to implement a system where a Library contains multiple Book objects is executed successfully.

