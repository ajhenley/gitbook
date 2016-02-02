###Using a Hashmap


{%ace edit=true, lang='java'%}
import java.util.HashMap;

public class HashmapApp
{
	public static void main( String[] args )
	{
		HashMap<String,String> map = new HashMap<String,String>();

		map.put( "cat", "Meow" );
		map.put( "pig", "Oink" );
		map.put( "dog", "Woof" );
		map.put( "bat", "Squeak" );
		
		System.out.println( "map = " + map );
		System.out.println();
		System.out.println("A cat says... " + map.get("cat"));
		System.out.println("A pig says... " + map.get("pig"));
		System.out.println("A dog says... " + map.get("dog"));
		System.out.println("A bat says... " + map.get("bat"));

	}
}
{%endace%}


