# RockPaperScissors
RPS
import java.util.Scanner;
import java.util.Random; 

public class RockPaperScissors {
	public static void main (String[] args) {
		String ComputerPlayer = "%s";
		int computerinput; 
		String PlayerInput;
		Scanner FirstPlay = new Scanner(System.in);
		Random Generate = new Random();
		
		System.out.println("Rock,Paper, Scissors! Type R,P,S");
		PlayerInput = FirstPlay.next();
		PlayerInput = PlayerInput.toUpperCase();
		computerinput = Generate.nextInt(3);
		if (computerinput == 0) 
			ComputerPlayer = "R";
		if (computerinput == 1)
			ComputerPlayer = "P";
		if (computerinput == 2)
			ComputerPlayer = "S";
		
	 System.out.printf("Computer Played:%s ", ComputerPlayer);
	if (PlayerInput.equals(ComputerPlayer))
		System.out.println("\n\n\nTie");
	//Winning Code
	else if (PlayerInput.equals("R") && ComputerPlayer.equals("S"))
		System.out.println("\n\n\nYou Win");
	else if (PlayerInput.equals("S") && ComputerPlayer.equals("P"))
		System.out.println("\n\n\nYou Win");
	else if (PlayerInput.equals("P") && ComputerPlayer.equals("R"))
		System.out.println("\n\n\nYou Win");
	//Losing Code
	else if (PlayerInput.equals("R") && ComputerPlayer.equals("P"))
		System.out.println("\n\n\nYouLose");
	else if (PlayerInput.equals("P") && ComputerPlayer.equals("S"))
		System.out.println("\n\n\nYouLose");
	else if (PlayerInput.equals("S") && ComputerPlayer.equals("R"))
		System.out.println("\n\n\nYouLose");
		//Invalid Entry
	else
		System.out.println("\n\n\nInvalid Entry: You Lose");
}

	} 
