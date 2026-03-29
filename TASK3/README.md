package internship;
import java.util.Scanner;
class BankAcc
{
	double balance = 1000;
	void deposit(double amt)
	{
		balance = balance + amt;
		System.out.println("The amount has been credicted to your account. ");
	}
	
	void withdraw(double amt)
	{
		if(amt <= balance)
		{
			balance = balance - amt;
			System.out.println("Transaction Successful. Kindly collect your cash.");
		}
		else
		{
			System.out.println("Unable to process the request. Insufficient Balance.");
		}
	}
	
	void checkBalance()
	{
		System.out.println("Your current account balance is: " + balance);
	}
}

public class Task3_ATM_Interface 
{
	public static void main(String[] args) 
	{
		Scanner sc = new Scanner(System.in);
		BankAcc account = new BankAcc();
		
		int ch=0;
		while(ch!=4)
		{
			System.out.println("\n---- ATM MENU ----");
			System.out.println("1. Check Balance");
			System.out.println("2. Deposit Money");
			System.out.println("3. Withdraw Money");
			System.out.println("4. Exit");
			System.out.print("Enter your choice: ");
			ch = sc.nextInt();
			
			switch(ch) {
			case 1:
				account.checkBalance();
				break;
			case 2:
				System.out.print("Enter amount to deposit: ");
				double deposit_amt = sc.nextDouble();
				account.deposit(deposit_amt);
				break;
			case 3:
				System.out.print("Enter amount to withdraw: ");
				double withdraw_amt = sc.nextDouble();
				account.withdraw(withdraw_amt);
				break;
			case 4:
				System.out.println("Thank you for using the ATM.");
				break;
			default:
				System.out.println("Invalid Choice. Please try once again.");
			}
		}
	}
}
