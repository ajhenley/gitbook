<!--djw:done-->
<!--ajh:done-->
By now, you should be comfortable with both writing programs and debugging programs (making a broken program work). This is a new type of assignment. Here we want to take a working program and change it to do something else.

{%ace edit=false, lang='java'%}
public class ChangeProgram {
	public static void main(String[] args) {
		int x, y, z;
		
		x = 5;
		y = 9;
		
		z = x * y;

		System.out.println("The product is " + z);
	}
}
{%endace%}

Change this program to output the product of 5 and 8.75.


<button class="section" target="section1" show="Sample Answer" hide="Hide Answer"></button>

<!--sec data-title="Answer" data-id="section1" data-show=false ces-->
{%ace edit=false, lang='java'%}
public class ChangeProgram {
    public static void main(String[] args) {
        int x;
        double y, z;

        x = 5;
        y = 8.75;

        z = x * y;

        System.out.println("The product is " + z);
    }
}
{%endace%}
<!--endsec-->