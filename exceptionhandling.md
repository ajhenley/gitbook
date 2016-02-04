###Exception Handling
####What is an excepction?
Definition: An exception is an event, which occurs during the execution of a program, that disrupts the normal flow of the program's instructions.

####So what am I supposed to do about it?
You have two choices. Handle it or throw it up the call stack.

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

 
After a method throws an exception, the runtime system attempts to find something to handle it. The set of possible "somethings" to handle the exception is the ordered list of methods that had been called to get to the method where the error occurred. The list of methods is known as the call stack.

The call stack showing three method calls, where the first method called has the exception handler.

 

The call stack.

The runtime system searches the call stack for a method that contains a block of code that can handle the exception. This block of code is called an exception handler.

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