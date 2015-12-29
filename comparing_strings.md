###Comparing strings
In Java ```ObjectA == ObjectB``` returns true when both objects share the same memory location. ```ObjectA.equals(ObjectB)``` also returns true when both objects share the same memory location. However, ```StringA.equals(StringB)``` returns true when the VALUE of ```StringA``` is the same as the VALUE of ```StringB```, regardless of memory location.

####Strings are different
Strings have a built-in method ```.equals()``` that compares itself to another String. The result is ```true``` if both strings contain the same content and ```false``` if they do not. Use the not operator ```!``` with the ```.equals()``` method to determine if two Strings are different.

Do you enjoy debugging and tracking down subtle errors? Do you like to bash your head against the wall while grinding your teeth and wailing uncontrollably? Then **don't use == to compare Strings for equality**. It might actually work sometimes for reasons buried deep inside the internals of Java. But if you value your sanity then use the ```.equals()``` method to compare Strings. Your head and teeth will thank you.

####Remember this:
The regular relational operators do not work with Strings.Only primitives.

####Do this:
Fix the following program so it works.Note: In order to keep you on your feet the complete program is not shown. Figure out the rest.

```java
    public static void main(String []args){
        Scanner sc = new Scanner(System.in);
        
        System.out.println("How is the weather?");
        String answer = sc.nextLine();
        
        if (answer.equals("rain"))
            System.out.println("Take your umbrella!");
        else if (answer == "windy")
            System.out.println("Wear your jacket!");
        else if (answer == "snow" )
            System.out.println("Wear a coat and take a shovel!");
        else
            System.out.println("Enjoy your day!");
     }
```





