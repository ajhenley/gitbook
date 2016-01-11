###Create book class
Congratulations. You've been hired to develop an application to manage an inventory of books.

Create a new project in Eclipse called BookApplication.
Right-click on your project and add a class.

Create a Book class that allows for the following fields: 
* Book title
* Author
* Description
* Price
* IsInStock

You'll start by creating the class and name it Book. All classes in Java begin with a capital letter.

Next, you'll add private member variables for each field above. You can't have spaces so name them accordingly. The first private member variable would probably be ```private String bookTitle```

Next, you'll create getters and setters for each field. The getters and setters for bookTitle look like this:

{%ace edit=true, lang='java'%}
public class Book {
	private String bookTitle;

	public String getBookTitle() {
		return bookTitle;
	}

	public void setBookTitle(String bookTitle) {
		this.bookTitle = bookTitle;
	}
}
{%endace%}

Notice that your Book class will not contain a method called main. That's because main is in a different part of your program. Main will call the Book class to create an object of type Book. Then we can populate the title by calling the setter and passing the bookTitle as a String.

{%ace edit=true, lang='java'%}
public class BookApplication {

	public static void main(String[] args) {
	
		Book myBook = new Book();
		myBook.setBookTitle("This Book Needs a Title");

	}
}
{%endace%}

Create a method that returns the pricing for a requested number of books. Five books at $20.00 should return $100, if they are in stock. If they are not in stock, that should be handled appropriately (hint - you decide).