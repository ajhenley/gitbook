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
