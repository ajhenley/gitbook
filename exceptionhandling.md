###Exception Handling
####What is an excepction?
Definition: An exception is an event, which occurs during the execution of a program, that disrupts the normal flow of the program's instructions. Short answer: It's an error!

####So what am I supposed to do about it?
You have two choices. Handle it or throw it up the call stack. We'll talk more about the call stack later. For now know that the call stack is a running list of the methods that have been called by your program. As each method finishes, control returns to the previous method.

After your method throws an exception, Java looks for someone to handle it. If you've written code that can handle it, great! You're talking to the manager on duty. Otherwise the exception says to your method: "I want to talk to they guy who hired you!". Put your ear to your computer. It literally says that. 

So the method that called your method gets the error. Can that method handle it? No? The exception goes up the call stack. Somebody is going to handle this error. Or this program will crash. And heads will roll.

Let's first look at some code that handles the exception on its own. This is easy - just surround the code that *could* cause an error with try..catch statements.

Here we consider the possibility that the file doesn't exist or isn't available. Since that is a likely possibility then let's give the user a "nice" message instead of crashing abruptly when that event occurs. Notice that we can have one to as many catch clauses as we like. We simply list them in order of most specific exception to most general exception.

{%ace edit=true, lang='java'%}
import java.io.*;
public class ExceptionExample {
//second commit
	public static void main(String[] args) {
		FileInputStream fis = null;
		int k;
		
		try
		{
			fis = new FileInputStream("c:\\myfile.txt");
						
			while ( (k = fis.read()) != -1)
			{
				System.out.println((char)k);
			}
		//catch the most specific exception first	
		}catch (FileNotFoundException e)
		{
			System.out.println("There is no file!");
		//an IO exception is more general... maybe the drive is corrupt
		}catch (IOException e)
		{
			System.out.println("There is an IO exception.");
		//This catches all the other exceptions that we can catch
		//So save the more general exception for last
		}catch (Exception e)
		{
		    System.out.println("Something else went wrong");
		}
	}
}
{%endace%}

There's one more thing I want to tell you that you can do with exceptions. You can give them away.





####What's the call stack? While you're at it... tell me about the heap
* Instance variables and objects live on the heap
* Local variables live on the stack

Huh? Stack and Heap are two places in memory. Your program consists of different things: mostly instance variables, objects and local variables.

If a local variable is an object (as the String object is below) it will be stored with other objects on the heap. However, the reference to it, the variable name containing a pointer to the object is stored on the stack. 

When you instantiate the Person class below by declaring ```Person p;``` the local variable p is stored on the stack. Once you instantiate the Person as ```p = new Person(); then p remains on the stack while the Person Ojbect is created on the heap.

public class Person {
    private String name;
    private int age;
    public String DisplayText();
}
        
        
Every method that is called in your program is listed in the call stack. 

Example application that handles exceptions: https://github.com/dave45678/ExceptionExample

Generally, when something is stored "on the stack", it has automatic storage duration, which means that it lives for the duration of the current function call. In contrast, when something is stored "on the heap", it has dynamic storage duration (hence allocating memory on the heap is called "dynamic memory allocation", http://en.wikipedia.org/wiki/Dyn...), which means it lives until we explicitly deallocate it, which can be as long or short as we want, and can live beyond the current function call. Dynamic memory allocation is more flexible, but is slower and you have to manage its duration manually.






How to Pass an Exception up the Call Stack

If a method needs to be able to throw an exception, it has to declare the exception(s) thrown in the method signature, and then include a throw-statement in the method. Here is an example:

    public void divide(int numberToDivide, int numberToDivideBy) throws BadNumberException{
        if(numberToDivideBy == 0){
            throw new BadNumberException("Cannot divide by 0");
        }
        return numberToDivide / numberToDivideBy;
    }
When an exception is thrown the method stops execution right after the "throw" statement. Any statements following the "throw" statement are not executed. In the example above the "return numberToDivide / numberToDivideBy;" statement is not executed if a BadNumberException is thrown. The program resumes execution when the exception is caught somewhere by a "catch" block.

How to Handle an Exception

If a method calls another method that throws checked exceptions, the calling method is forced to either pass the exception on, or catch it. Catching the exception is done using a try-catch block. Here is an example:

    public void callDivide(){
        try {
            int result = divide(2,1);
            System.out.println(result);
        } catch (BadNumberException e) {
            //do something clever with the exception
            System.out.println(e.getMessage());
        }
        System.out.println("Division attempt done");
    }
The BadNumberException parameter e inside the catch-clause points to the exception thrown from the divide method, if an exception is thrown.

 

Finally

You can attach a finally-clause to a try-catch block. The code inside the finally clause will always be executed, even if an exception is thrown from within the try or catch block. If your code has a return statement inside the try or catch block, the code inside the finally-block will get executed before returning from the method. Here is how a finally clause looks:

    public void openFile(){
        FileReader reader = null;
        try {
            reader = new FileReader("someFile");
            int i=0;
            while(i != -1){
                i = reader.read();
                System.out.println((char) i );
            }
        } catch (IOException e) {
            //do something clever with the exception
        } finally {
            if(reader != null){
                try {
                    reader.close();
                } catch (IOException e) {
                    //do something clever with the exception
                }
            }
            System.out.println("--- File End ---");
        }
    }
No matter whether an exception is thrown or not inside the try or catch block the code inside the finally-block is executed. The example above shows how the file reader is always closed, regardless of the program flow inside the try or catch block.

List of Available Exceptions

http://docs.oracle.com/javase/7/docs/api/java/lang/Exception.html

 

The Call Stack Explained

This text refers to the concept the "call stack" in several places. By the call stack is meant the sequence of method calls from the current method and back to the Main method of the program. If a method A calls B, and B calls C then the call stack looks like this:

    A
    B
    C
When method C returns the call stack only contains A and B. If B then calls the method D, then the call stack looks like this:

    A
    B
    D
Understanding the call stack is important when learning the concept of exception propagation. Exception are propagated up the call stack, from the method that initially throws it, until a method in the call stack catches it. More on that later.

You might be wondering whether you should catch or propogate exceptions thrown in your program. It depends on the situation. In many applications you can't really do much about the exception but tell the user that the requested action failed. In these applications you can usually catch all or most exceptions centrally in one of the first methods in the call stack. You may still have to deal with the exception while propagating it though (using finally clauses). For instance, if an error occurs in the database connection in a web application, you may still have to close the database connection in a finally clause, even if you can't do anything else than tell the user that the action failed.