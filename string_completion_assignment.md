<!--djw:done-->
<!--ajh:done-->
###String completion assignment

The following code is supposed to ask the user their pet's name, breed and age. Add the 3 lines necessary to make this work...

{%ace edit=false, lang='java'%}
 import java.util.Scanner;
  
 public class PetQuestions
 {
     public static void main( String[] args )
    {
        String name;
        String breed;
        int age;

        System.out.print( "Greetings. What is your pet's name? " );
        name = keyboard.next();
 
        System.out.print( "What kind of animal is " + name + "? " );
        System.out.print( "How old is " + name + "? ");
        
        System.out.println( name + " is your " + breed + " and it is " + age );
     }
 }
{%endace%}


<button class="section" target="section1" show="Sample Answer" hide="Hide Answer"></button>

<!--sec data-title="Answer" data-id="section1" data-show=false ces-->
{%ace edit=false, lang='java'%}
import java.util.Scanner;

public class PetQuestions {
	public static void main(String[] args) {
        String name;
        String breed;
        int age;

        Scanner keyboard = new Scanner(System.in);
        
        System.out.print( "Greetings. What is your pet's name? " );
        name = keyboard.next();
 
        System.out.print( "What kind of animal is " + name + "? " );
        breed =keyboard.next();
        
        System.out.print( "How old is " + name + "? ");
        age = keyboard.nextInt();
        
        System.out.println( name + " is your " + breed + " and it is " + age );
	}
}
{%endace%}
<!--endsec-->