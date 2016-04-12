<!-- djw: done -->
<!--ajh:done-->
###Special characters assignment

Sadly, this application doesn't work... but you're the person who can fix it.

{%ace edit=false, lang='java'%}
public class SpecialCharacterProgram {
    String message1, message2;
    
    message1 = \/\/\/\/\/\r\t\b
    message2 = ";
    
    System.out.println(message1 + message2);
            
}
{%endace%}

This is more difficult than you think unless you work through it methodically. 
Fix the variables message1 and message2 so the program prints the following:

```
message1 = \/\/\/\/\/\r\t\b
message2 = ";
```

You should not add any new lines of code. In other words, do not add additional System.out.println() statements. You can do it. The world believes in you!


<button class="section" target="section1" show="Sample Answer" hide="Hide Answer"></button>

<!--sec data-title="Answer" data-id="section1" data-show=false ces-->
{%ace edit=false, lang='java'%}
public class SpecialCharacters {
	public static void main(String[] args) {
	    String message1, message2;

	    message1 ="message1 = \\/\\/\\/\\/\\/\\r\\t\\b ";
	    message2 = "\nmessage2 = \";";

	    System.out.println(message1 + message2);
	}
}
{%endace%}
<!--endsec-->

Need it explained? Then watch the video walkthrough...<br />
[Video Walkthrough - http://links.learningbycoding.com/specialchars](https://ajhenley.wistia.com/medias/hgvfnibluf)