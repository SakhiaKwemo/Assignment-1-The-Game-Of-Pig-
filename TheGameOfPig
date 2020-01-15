//Sakhia.Kelil.Kwemo                NetId: 16skk1                   Student Number: 20059325

import java.util.Random;
import java.util.Scanner;

public class Assn1_16skk1 {
	
	static Random generator = new Random(System.currentTimeMillis());   
	public static final Scanner play = new Scanner(System.in);
	public static void main(String[] args) {
		int lastgameC = 0;
		int lastgameP = 0;
		int gameP = 0;
		int gameC = 0; 
		int sumP = 0;
		int sumC = 0;
		System.out.println("Welcome to The Game Of Pig");
		System.out.println("When its your turn press 1 to roll the dice");
		while(true) {
			
			System.out.println("Player's turn: ");
			int roll = play.nextInt();
			while(roll == 1) {
			
				
				int x = generator.nextInt(5)+1;
				int y = generator.nextInt(5)+1;
				String dice1 = diceName(x);
				String dice2 = diceName(y);
				System.out.println("Player rolled a " +dice1+ " + " +dice2);
				if(x == 1 || y == 1) {
					
					if (x != y) {
						System.out.println("TURN OVER! Turn sum is zero!\n");
						sumP = 0; 
						gameP = lastgameP;
					break; 
					}
				
					else {
						System.out.println("Double Ones!");
						sumP = 25;
						gameP += sumP; 	
						System.out.println("Player's turn sum is: " +sumP+ "  and game sum would be: " +gameP);
						if (RollAgain() == true) {
							continue; 
						}
						else {
							break; 
						}
					}
				}
				else if(x == y) {
					System.out.println("Doubles!");
					sumP = x*4;
					gameP += sumP; 
					System.out.println("Player's turn sum is: " +sumP+ "  and game sum would be: " +gameP);
					if (RollAgain() == true) {
						continue; 
					}
					else {
						break; 
					}
				}
				else if(x != y) {
						
					sumP = x+y; 	
					gameP += sumP; 
					System.out.println("Player's turn sum is: " +sumP+ "  and game sum would be: " +gameP);
					if (RollAgain() == true) {
						continue; 
					}
					else {
						
						break; 
					}
				}
			
			}
		System.out.println("Player's sum is: " +gameP+ ",  Compuer's sum is: \n" +gameC);
		lastgameP = gameP;
		if (gameP > 100) {
			break;
		}
			
			System.out.println("Computer's turn: ");
			
			while(true) {
				int x = generator.nextInt(5)+1;
				int y = generator.nextInt(5)+1;
				String dice1 = diceName(x);
				String dice2 = diceName(y);
				System.out.println("Computer rolled a " +dice1+ " + " +dice2);
				if(x == 1 || y == 1) {
					
					if (x != y) {
						System.out.println("TURN OVER! Turn sum is zero!\n");
						sumC = 0; 
					break; 
					}
				
					else {
						System.out.println("Double Ones!");
						sumC = 25;
						gameC += sumC; 	
						System.out.println("Computer's turn sum is: " +sumC+ "  and game sum would be: " +gameC);
						if (generator.nextInt(2) == 1) {
							continue; 
						}
						else {
							break; 
						}
					}
				}
				else if(x == y) {
					System.out.println("Doubles!");
					sumC = x*4;
					gameC += sumC; 	
					System.out.println("Computer's turn sum is: " +sumC+ "  and game sum would be: " +gameC);
					if (generator.nextInt(1) == 1) {
						continue; 
					}
					else {
						break; 
					}
				}
				else if(x != y) {
						
					sumC = x+y;
					gameC += sumC; 	
					System.out.println("Computer's turn sum is: " +sumC+ "  and game sum would be: " +gameC);
					if (generator.nextInt() == 1) {
						continue; 
					}
					else {
						
						break; 
						
					}
				}
			
			}
		System.out.println("Player's sum is: " +gameP+ ",  Compuer's sum is: \n" +gameC);
		if (gameC > 100) {
			break;
		}
		}
		Winner(gameP, gameC);
	}

	public static String diceName(int b) {
		
		
		String dice = null;
		if(b == 1) {
			dice = "one";
		}	
		else if(b == 2) {
			dice = "two";
		}
		else if(b == 3) {
			dice = "three";
		}
		else if(b == 4) {
			dice = "four";
		}	
		else if( b == 5) {
			dice = "five";
		}	
		else if(b == 6) {
			dice = "six";
		}
	return dice;
	}
	
	public static boolean RollAgain() {
		
		Scanner reader = new Scanner(System.in);
		System.out.println("Do you want to go again? Press (y/n): ");
		String playerchoice = reader.next();
		if(playerchoice.contentEquals("y")) {
			
			return true;
		}
		else {
			return false; 
		}
	}
	
	public static void Winner(int x, int y) {
		
		if(x > y) {
			System.out.println("You are the Winner!!!");
		}
		else {
			System.out.println("The Computer is the Winner!!!");
		}
	}
		
}
