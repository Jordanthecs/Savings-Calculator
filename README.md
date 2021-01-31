# Savings Calculator

import java.util.Scanner;//gets user input

public class savingCalculator {//class name is savingCalculator

	public static void main(String[] args) {// main method
		
		Scanner userInput = new Scanner(System.in);// scanner name is now userInput
		Scanner userDoubleInput = new Scanner(System.in);
			
		System.out.println("Do you want to calculate your savings? (1 for yes or 2 for no)");
		
		int calc = userInput.nextInt();
		
		while(calc < 1 || calc > 2) {
			System.out.println("Choose either 1 or 2.");
			calc = userInput.nextInt();
		}
		
		while(calc == 1) {
		
	
			System.out.println("Which option would you like to know?");//prompts user to make chose a decision
			System.out.println("1. How many months it will take you to save your goal?");// 1 tells you how many months it will take to save a certain amount
			System.out.println("2. How much money you will have saved up in a certain amount of months?");//2 tell you how much money you will have saved by the a certain amount of months
			
			int choice = userInput.nextInt();
			
			while(choice < 1 || choice > 2) {
				System.out.println("Choose either 1 or 2.");
				choice = userInput.nextInt();
			}
			
			
			
			
			if(choice == 1){// if user chooses 1, this will run
				System.out.println("How much money do you have saved up?");
				int moneySaved = userInput.nextInt();// gets the amount already saved
		
				System.out.println("How much money are you saving every month?");
				int moneyAdded = userInput.nextInt();// gets the amount that will be saved each month
		
				System.out.println("What is your savings goal?");
				int goal = userInput.nextInt();// gets the saving goal
		
				double monthsNeeded = ((goal-moneySaved)/moneyAdded);// the saving goal divided by the amount saved each month tells you how many months it will take to reach the goal
				if (monthsNeeded >12) {
				System.out.println("It will take you "+ monthsNeeded/12 +" years to save up $"+ goal);// prints out the result
				
				System.out.println("Do you want to calculate your savings? (1 for yes or 2 for no)");
				
				calc = userInput.nextInt();
				
				
				}else {
					System.out.println("It will take you "+ monthsNeeded +" months to save up $"+ goal);// prints out the result
					
					System.out.println("Do you want to calculate your savings? (1 for yes or 2 for no)");
					
					calc = userInput.nextInt();
					
				}
			}else if (choice ==2){// if user chooses 1, this will run
				System.out.println("How much money do you have saved up?");
				int moneySaved = userInput.nextInt();
			
				System.out.println("How much money are you saving every month?");
				int moneyAdded = userInput.nextInt();
			
				System.out.println("How many months are you saving for?");
				double monthsSaving = userDoubleInput.nextDouble();// gets how many month the user is saving for
			
				double moneyAfterMonths = (monthsSaving* moneyAdded) + moneySaved;//multiplies the months of saving by the amount saved every month and add the amount already saved for the result
			
				System.out.println("You will have $"+ moneyAfterMonths + " after "+ monthsSaving+" months!");// prints result
				
				System.out.println("Do you want to calculate your savings? (1 for yes or 2 for no)");
				
				calc = userInput.nextInt();
				
			}

		} 
	}
	
}
