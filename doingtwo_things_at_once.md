# Doing two things at once

Complete the following program and run three threads . Make the message from each thread unique. What do you see?.

{%ace edit=true, lang='java'%}
package multiThread;

import xxxxxx;

/**   A runnable that repeatedly prints a greeting.  */
public class  NameofRunnable implements Runnable {      
/*   class variables and methods   */
 
	/**  Constructs the runnable object.  *  @param aGreeting            the greeting to display  */
	public NameofRunnable (String aGreeting) ) {
 	}
	public void run() {
	try {
	  for (int i = 1; i &lt;= REPETITIONS; i++) {
	   Date now = new Date();
	System.out.println(now + " " + greeting);
	Thread.sleep(DELAY);
 
	}
	} catch (InterruptedException exception) 
	{
                            }
                   }

public static void main(String[] args) {
 
	/*** run threads */

}
}
{%endace%}


