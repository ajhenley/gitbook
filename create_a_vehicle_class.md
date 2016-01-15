###Create an abstract vehicle class
Modify your Car Class application. Now you will create an abstract class for a Vehicle. The Vehicle can run, stop and accelerate. However the abstract class can not fly like a plane or float like a boat. Nor can it haul 10 tons of gravel like the dump truck that just dinged my windshield. Specific implementations are created by inheriting your abstract class. To do that we use the keyword ```extends```. Then you can create a Plane class, a Boat class and a Car class. Each subclass will inherit from the Vehicle class. Any method the vehicle has will be available to the Plane, Boat or Car. Methods you add to the Plane, Boat or Car are specific to that type of Vehicle.

####Preventing Inheritance
You can make your Plane, Boat and Car implementations final by using the keyword final after the modifier public in the class definition. Final classes can't be inherited. This isn't common but you may sometimes see people do this. Also, you can prevent a specific method from being overridden in the same way.

Note: If a constructor does not explicitly invoke a superclass constructor, the Java compiler automatically inserts a call to the no-argument constructor of the superclass. If the super class does not have a no-argument constructor, you will get a compile-time error. Object does have such a constructor, so if Object is the only superclass, there is no problem.

####Example Abstract Class
{%ace edit=true, lang='java'%}
public abstract class Message
{
	private String sender;
    private String receiver;
	
	public String getSender() {
		return sender;
	}

	public void setSender(String sender) {
		this.sender = sender;
	}

	public String getReceiver() {
		return receiver;
	}

	public void setReceiver(String receiver) {
		this.receiver = receiver;
	}
    abstract String SubmitContent(); //an abstract method
}
{%endace%}

{%ace edit=true, lang='java'%}

public class EmailMessage extends Message{
    private String messageBody;

    
	public String getMessageBody() {
		return messageBody;
	}

	public void setMessageBody(String messageBody) {
		this.messageBody = messageBody;
	}

	@Override
	String SubmitContent() {
		String status = "";
		status = SendEmail(getSender(),getReceiver(), getMessageBody());
		return status;
	}

	private String SendEmail(String sender, String receiver, String messageBody2) {
		// code to send the email and set return status goes here
		return "Message Sent";
	}
    
    
}
{%endace%}

