# Converting-Binary-code
This project about convert a string in binary code easily.
package project2;
import java.util.Scanner;
public class Nice {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		String s="";

        s+=sc.nextLine();
       
        sc.close();
		  byte[] bytes = s.getBytes();
		  StringBuilder binary = new StringBuilder();
		  for (byte b : bytes)
		  {
		     int val = b;
		     for (int i = 0; i < 8; i++)
		     {
		        binary.append((val & 128) == 0 ? 0 : 1);
		        val <<= 1;
		     }
		     binary.append(" ");
		  System.out.println( binary);
	}

	}
}
