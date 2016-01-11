###Create book class
Congratulations. You've been hired to develop an application to manage an inventory of books.

Create a new project in Eclipse called BookApplication.
Right-click on your project and add a class.

Create a Book class that allows for the following fields: 
* SKU (stockkeeping unit - will serve as unique ID for each book)
* Book title
* Author
* Description
* Price
* IsInStock

You'll start by creating a project in Eclipse called BookApplication.

Your book application will need a class. Create a class and name it Book. All classes in Java begin with a capital letter.

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

Notice that your Book class will not contain a method called main. That's because main is in a different part of your program. You'll see that in the upcoming assignment to create a book app. 

Main will call the Book class to create an object of type Book. Then we can populate the title by calling the setter and passing the bookTitle as a String.

{%ace edit=true, lang='java'%}
public class BookApplication {

	public static void main(String[] args) {
	
		Book myBook = new Book();
		myBook.setBookTitle("This Book Needs a Title");

	}
}
{%endace%}

Create a method that returns the pricing for a requested number of books. Five books at $20.00 should return $100, if they are in stock. If they are not in stock, that should be handled appropriately (hint - you decide).

Finally, create a constructor. The constructor is a method with the same name as the class. When an object is instantiated using the keyword 'new' the constructor will always be called. For this reason the constructor can be used to initialize your variables. Set each private memeber variable to an appropriate initial value. That would be an empty string for text and 0.0 for numeric values.



###Enhancing your book class
The Book class already contains private member variables and a default constructor. It also contains getters and setters for each private member variable.

Next, you'll add an overloaded constructor and a method.

An overloaded constructor is a constructor that takes one or more parameters. Create one that takes an SKU and returns the appropriate book object.

Next, create a method called getDisplayText(). It takes no parameters. When called it returns a string containing the author, title and description. You'll use this method to print your book information to the console.

