# What does this code do? Part 1

/*
 * Eden Ghirmai
 * CheckPalindrome.java
 * 
 * Checks if the string entered by the user is a palindrome. 
 * That is that it reads the same forwards as backwards like "racecar"
 */

import java.util.*;

public class CheckPalindrome {
	public static void main(String[] args) {
		// Data will come from the user at the keyboard
		Scanner in = new Scanner(System.in);
		
		System.out.println("Palindrome Checker");
		System.out.print("What phrase would you like to check? ");
		String original = in.nextLine();
		
		// Convert to lower case to simplify comparing strings
		String phrase = original.toLowerCase(); 
		
		String backwards = ""; 
		
		// loop through the string backwards, starting with the last character
		for (int i = phrase.length() - 1; i >= 0; i--) {
		
		    // Extract each letter as the next character 
		    // and build the backwards string
			String letter = phrase.substring(i, i + 1);
			backwards += letter;
		}		
		
		// A palindrome is a word or phrase that is the same forward or 
		// backward. This is where we check that.
		if (phrase.equals(backwards)) {
			System.out.println(original + " is a palindrome!");
		} else {
			System.out.println(original + " is not a palindrome!");			
		}
		
	}
}
