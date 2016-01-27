###Composition vs Inheritance Explained
Both composition and inheritance enable a class to reuse the code of another class. Programmers may use inheritance to get one class to contain the functionality of another. Sometimes that's the best idea in the world. Sometimes it's a square wheel. Which to use and when? The correct answer depends on the relationship between the classes.

With Composition you learned how a Person class could have a Job. Or an Education class could contain schools. We call these *has-a* relationships because the first class *has-an* object of the second class. 

Inheritance is the other type of relationship. It occurs when one class inherits another. An Employee class is a more specific instance of a Person. It inherits the Person class. This type of relationship is called an *is-a* relationship. All the attributes of Person are in Employee as well as some attributes specific to Employees. Such as Department, JobTitle, PayRate, etc... 

###How to implement Inheritence
Here's an example with an Instrument and a Saxophone. Notice that the Instrument does not know anything about the Saxophone. The Instrument is a class that existed when the developer discovered the need for a more specific instrument. 

{%ace edit=true, lang='java'%}
public Instrument(){
		System.out.println("An instrument is created");
	}
	public Instrument(String classification,String name, int yearInvented){
		this.classification = classification;
		this.name = name;
		this.yearInvented = yearInvented;
	}
	
	public void play(){
		System.out.println("The instrument is playing");
	}
	public void tune(){
		System.out.println("The instrument is being tuned");
	}
	public String getClassification() {
		return classification;
	}
	public void setClassification(String classification) {
		this.classification = classification;
	}
	public String getName() {
		return name;
	}
	public void setName(String name) {
		this.name = name;
	}
	public int getYearInvented() {
		return yearInvented;
	}
	public void setYearInvented(int yearInvented) {
		this.yearInvented = yearInvented;
	}
	
}
{%endace%}

{%ace edit=true, lang='java'%}

public class Saxophone extends Instrument{
	private String mouthpiece;
	private String key;
	private String material;//brass or nickel
	private String range; // alto, tenor, baritone
	
	public Saxophone(){
	    //call the constructor of the super class
		super("woodwind","saxopone",1840);
	}
	public String getMouthpiece() {
		return mouthpiece;
	}
	public void setMouthpiece(String mouthpiece) {
		this.mouthpiece = mouthpiece;
	}
	public String getKey() {
		return key;
	}
	public void setKey(String key) {
		this.key = key;
	}
	public String getMaterial() {
		return material;
	}
	public void setMaterial(String material) {
		this.material = material;
	}
	public String getRange() {
		return range;
	}
	public void setRange(String range) {
		this.range = range;
	}
	public void replaceReed(){
		System.out.println("Gotta new reed and ready to boogie!");
	}
	public void tune(){
		System.out.println("An out-of-tune sax sounds like a cat fight" );
	}

}
{%endace%}

###What You Should Do Now
Create an Employee class and make it extend the Person class. Your employee class should include fields for Department, JobTitle and PayRate. 
Create a ```toString()``` override for both Job and Education that outputs the information in the class to the console. The ```toString()``` override for Person should use the ```toString()``` methods for the Job and Education member objects.


