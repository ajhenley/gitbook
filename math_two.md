<!--djw:done-->
<!--ajh:done-->
###Math two
Write an application that assigns 2 to a variable named ```mynumber``` and 1.7938 to a variable named ```myothernumber```, and then prints out the values to the console.


<button class="section" target="section1" show="Sample Answer" hide="Hide Answer"></button>

<!--sec data-title="Answer" data-id="section1" data-show=false ces-->
{%ace edit=false, lang='java'%}
public class MathTwoProg {
    public static void main(String[] args) {
        int myNumber;
        double myOtherNumber;

        myNumber = 2;
        myOtherNumber = 1.7938;

        System.out.println("myNumber is " + myNumber);
        System.out.println("myOtherNumber is " + myOtherNumber);
    }
}
{%endace%}
<!--endsec-->