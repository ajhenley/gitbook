# Object-Oriented Java Solutions

##Create Book Class

```java
public class Book {
	private String author;
	private int pageCount;
	private double price;
	private String title;

	public Book() {
		author = "";
		price = 0.0;
		pageCount = 0;
		title = "";
	}
	public Book(String value , double price1 ,int page_count ,String title1)
	{
		author =value;
		price = price1;
		pageCount = page_count;
		title =title1;
	}
	
	public void setAuthor(String value)
	{
		this.author =value;
	}
    
	public String getAuthor()
	{
		return author;
	}
    
	public void setPrice(double price1)
	{
		this.price =price1;
	}
    
	public double getPrice()
	{
		return price;
	}
	
	public void setPageCount(int pages)
	{
		this.pageCount = pages;
	}
	public int getPageCount()
	{
		return pageCount;
	}
	
	public void setTitle(String title1)
	{
		this.title= title1;
	}
	
	public String getTitle()
	{
		return title;
	}
}
```


##Create Book Database

```java
public class BookDB {

	public static Book getBook(String value) {

		Book b = new Book();
		switch (value) {

		case "Java1001":
			b.setSku("Java1001");
			b.setTitle("Head First Java");
			b.setAuthor("Kathy Sierra and Bert Bates");
			b.setDescription("Easy to read java workbook");
			b.setPrice(47.50);
			b.setIsInStock(true);

			break;

		case "Java1002":
			b.setSku("java1002");
			b.setTitle("Thinking in Java");
			b.setAuthor("Bruce Eckel");
			b.setDescription("Details about Java under the hood");
			b.setPrice(20.00);
			b.setIsInStock(false);

			break;

		case "Orcl1003":
			b.setSku("Orcl1003");
			b.setTitle("OCP: Oracle Certified Professional Java SE");
			b.setAuthor("Jeanne Boyarsky");
			b.setDescription("Everything you need to know in one place");
			b.setPrice(45.00);
			b.setIsInStock(true);

			break;

		case "Python1004":
			b.setSku("Python1004");
			b.setTitle("Automate the Boring Stuff with Python");
			b.setAuthor("Al Sweigart");
			b.setDescription("Fun with Python");
			b.setPrice(10.50);
			b.setIsInStock(true);

			break;

		case "Zombie1005":
			b.setSku("Zombie1005");
			b.setTitle("The Maker's Guide to the Zombie Apocalypse");
			b.setAuthor("Simon Monk");
			b.setDescription("Defend Your Base with Simple Circuits, Arduino, and Raspberry Pi");
			b.setPrice(16.50);
			b.setIsInStock(true);

			break;

		case "Rasp1006":
			b.setSku("Rasp1006");
			b.setTitle("Raspberry Pi Projects for the Evil Genius");
			b.setAuthor("Donald Norris");
			b.setDescription("A dozen fiendishly fun projects for the Raspberry Pi!");
			b.setPrice(14.75);
			b.setIsInStock(true);

			break;

		default:
			throw new IllegalArgumentException("Book not found: ");
		}
		return b;
	}
}
```