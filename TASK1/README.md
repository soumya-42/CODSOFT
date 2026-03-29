package internship;
import java.util.*;
public class Task1_Number_Game 
{
	public static void main(String[] args) 
	{
		Random random = new Random();
		Scanner sc = new Scanner(System.in);
		int num = random.nextInt(100)+1;
		int guess = 0;
		int attempt = 0;
		System.out.println("Number Guess Game...");
		System.out.println("Can you guess the number(1-100): ");
		
		while(guess!=num)
		{
			System.out.print("What's your guess: ");
			guess = sc.nextInt();
			attempt++;
			
			if(guess==num)
			{
				System.out.println("Great!!!! That's the correct number...");
				System.out.println("Total Attempts are: " + attempt);
			}
			
			else if(guess>num)
			{
				System.out.println("Too High! Try once more.");
			}
			
			else
			{
				System.out.println("Too Small! Try guessing another number.");
			}
		}
	}
}
