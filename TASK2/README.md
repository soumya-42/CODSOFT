package internship;
import java.util.Scanner;
public class Task2_Student_Grade_Calculator 
{
	public static void main(String[] args) 
	{
		Scanner sc = new Scanner(System.in);
		System.out.print("Enter total number of subjects: ");
		int sub = sc.nextInt();
		int overallmarks = 0;
		for(int i=1;i<=sub;i++)
		{
			System.out.print("Enter the marks obtained in subject " + i + ": ");
			int marks = sc.nextInt();
			overallmarks = overallmarks + marks;
		}
		double avg = (double) overallmarks/sub;
		char grade;
		if(avg>=90)
			grade = 'A';
		else if(avg>=80)
			grade = 'B';
		else if(avg>=70)
			grade = 'C';
		else if(avg>=60)
			grade = 'D';
		else
			grade = 'F';
		
		System.out.println("Total Marks: " + overallmarks);
		System.out.println("Average Percentage: " + avg);
		System.out.println("Grade Scored: " + grade);
	}
}
