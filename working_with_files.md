###Working with files
Sometimes you want to save data to work with another day. Or to share between sytems. That's when you save your data to a file or database. We'll look at databases later. For now, let's write and read to a file.

The following application will prompt the user to enter their favorite movies. When they are done it will list the movies. Each movie will be saved to a file so that the program can be run another day and keep track of all the movies.

The File class is used to create files and directories. The methods of the File class can be used to delete or rename files. It can also be used to see if a file exists.

An object of type File is used to represent either a file or a directory.

{%ace edit=true, lang='java'%}
import java.util.Scanner;
import java.io.PrintWriter;
import java.io.IOException;
import java.io.File;
import java.io.BufferedReader;
import java.io.FileReader;

public class WorkingWithFiles {

	public static void main(String[] args)
	{
		try {
			
			// If movies does not exist no file is  created, if movies
			// does exist then the new File object points to the existing
			// file
			File file = new File("movies");		
			file.createNewFile();
			
			//write some data to the file
			PrintWriter pw = new PrintWriter(file);
			
			Scanner keyboard = new Scanner(System.in);
			System.out.print("Enter the name of your favorite movies.");
			System.out.println("Press 'q' to quit:");
			String result = keyboard.nextLine();
			if (!result.equals("q")){
				pw.println(result);
			}
			
			while(!result.equals("q"))
			{
				result = keyboard.nextLine();
				pw.println(result);
			}
			pw.flush();
			pw.close();
			
			//read our file
			FileReader fr = new FileReader(file);
			BufferedReader br = new BufferedReader(fr);
			String line;
			while ( (line = br.readLine())!= null)
			{
				System.out.println(line);
			}
			br.close();
			
			
		} catch (IOException e) {
			System.out.println("Oops! An error occurred.");
		}
	}
}
{%endace%}

####Your assignment
Create a program that will prompt for 15 temperatures and save the temperatures to a file. Then read the temperatures from the file.

