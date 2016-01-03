<!--djw:done-->
<!--ajh:done-->
###Debug this program
This program is trying to assign two values to two variables, but if you put it in Eclipse it won't successfully run. Find and fix the error.
{%ace edit=false, lang='java'%}
public class DebugProg {
	public static void main(String[] args) {
		int x, y;
		
		x = 3.1415;
		y = 3.64;
		
		System.out.println("pi is approximately " + x);
		System.out.println("My GPA was " + y);
	}
}
{%endace%}


<button class="section" target="section1" show="Sample Answer" hide="Hide Answer"></button>

<!--sec data-title="Answer" data-id="section1" data-show=false ces-->
{%ace edit=false, lang='java'%}
public class DebugProg {
    public static void main(String[] args) {
        double x, y;

        x = 3.1415;
        y = 3.64;

        System.out.println("pi is approximately " + x);
        System.out.println("My GPA was " + y);
    }
}
{%endace%}
<!--endsec-->