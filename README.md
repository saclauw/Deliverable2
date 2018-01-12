import java.util.Scanner;
import java.text.SimpleDateFormat;

public class Deliverables2 {
public static void main(String [] args) {   

	Scanner scnr = new Scanner(System.in); 


		System.out.println("Please enter a date in the following format MM/DD/YYYY: " );
		System.out.println("");
		String dateOne = scnr.nextLine();
		
		/*
		 * This application is probably a lot more convoluted than it has to be, and also still has it flaws.
		 * I tried to utilize Simple Date, but couldn't get the results I wanted so I did a manual calculation
		 * to get the duration between the two dates.  I didn't factor in leap year... but I was able to account
		 * for the difference in number of days in months.
		 * 
		 * Had a lot of issues with validating the user input.  I am not sure where I went wrong, but it kept producing errors
		 * I had other validations, but they were holding up the application
		 * examples of other input validations:
		 * 
		 * 	while (dateOne.length() != 9) {   // This was supposed to only allow strings with char length of 10 chars
		 * 		if (dateOne.length() != 9) {
		 *		System.out.println("Not a valid entry.  Please reenter date in the following format MM/DD/YYYY:");
		 *		System.out.println("");
		 *		dateOne = scnr.nextLine(); } }   
		 *
		 *  while (dateOne.charAt(0) > 1 { // This was supposed to only allow the month input to begin with a char 0 or 1
		 *  		if (dateOne.charAt(0) >1 { 
		 *  		System.out.println("Not a valid entry.  Please reenter date in the following format MM/DD/YYYY:");
		 *		System.out.println("");
		 *		dateOne = scnr.nextLine(); } }   
		 *
		 *	while (dateOne.charAt(3) > 3 { // This was supposed to limit the days to be being beneath 40
		 *		if (dateOne.charAt(3) > 3 {
		 *		System.out.println("Not a valid entry.  Please reenter date in the following format MM/DD/YYYY:");
		 *		System.out.println("");
		 *		dateOne = scnr.nextLine(); }}
		 *
		 */
		
		while ((dateOne.charAt(2) != 47) && (dateOne.charAt(5) != 47)) {   // This ensures that character 3 and 6 are "/" in input 1
			if ((dateOne.charAt(2) != 47) && (dateOne.charAt(5) != 47)) {
				System.out.println("Not a valid entry.  Please reenter date in the following format MM/DD/YYYY:");
				System.out.println("");
				dateOne = scnr.nextLine(); } }
		
		
		System.out.println("");
		System.out.println("You entered the following date: " + dateOne);
		System.out.println("");
		
		System.out.println("Please enter a second date following the same format MM/DD/YYYY: " );
		System.out.println("");
		String dateTwo = scnr.nextLine();
		
	
		while ((dateTwo.charAt(2) != 47) && (dateTwo.charAt(5) != 47)) {  // This ensures that character 3 and 6 are "/" in input 2
			if ((dateTwo.charAt(2) != 47) && (dateTwo.charAt(5) != 47)) {
				System.out.println("Not a valid entry.  Please reenter date in the following format MM/DD/YYYY:");
				System.out.println("");
				dateTwo = scnr.nextLine(); } }
	
		System.out.println("");
		System.out.println("You entered the following date: " + dateTwo);
		System.out.println("");
		System.out.println("The two dates you have entered are: " + dateOne + " & " + dateTwo);
		System.out.println("");
		
		
	    char yr1Dig1 = dateOne.charAt(6);    //This is converting the chars in the string into int values for the year in input 1
	    int y1D1 = Character.getNumericValue(yr1Dig1);
	    char yr1Dig2 = dateOne.charAt(7);
	    int y1D2 = Character.getNumericValue(yr1Dig2);
	    char yr1Dig3 = dateOne.charAt(8);
	    int y1D3 = Character.getNumericValue(yr1Dig3);
	    char yr1Dig4 = dateOne.charAt(9);
	    int y1D4 = Character.getNumericValue(yr1Dig4);
	    int year1Full = (y1D1 * 1000) + (y1D2 * 100) + (y1D3 * 10) + y1D4;
	    
	    char yr2Dig1 = dateTwo.charAt(6);
	    int y2D1 = Character.getNumericValue(yr2Dig1);   //This is converting the chars into int values for the year in input 2
	    char yr2Dig2 = dateTwo.charAt(7);
	    int y2D2 = Character.getNumericValue(yr2Dig2);
	    char yr2Dig3 = dateTwo.charAt(8);
	    int y2D3 = Character.getNumericValue(yr2Dig3);
	    char yr2Dig4 = dateTwo.charAt(9);
	    int y2D4 = Character.getNumericValue(yr2Dig4);
	    int year2Full = (y2D1 * 1000) + (y2D2 * 100) + (y2D3 * 10) + y2D4;
	    
	    
	   // System.out.println("Year 1 = " + year1Full + " & Year 2 = " + year2Full);
	    
	    char mnth1Dig1 = dateOne.charAt(0);  //This is converting the chars into the int values for the month in input 1
	    int m1D1 = Character.getNumericValue(mnth1Dig1);
	    char mnth1Dig2 = dateOne.charAt(1);
	    int m1D2 = Character.getNumericValue(mnth1Dig2);
	    int month1Full = (m1D1 * 10) + m1D2;
	    
	    char mnth2Dig1 = dateTwo.charAt(0); //This is converting the chars into the int values for the month in input 2
	    int m2D1 = Character.getNumericValue(mnth2Dig1);
	    char mnth2Dig2 = dateTwo.charAt(1);
	    int m2D2 = Character.getNumericValue(mnth2Dig2);
	    int month2Full = (m2D1 * 10) + m2D2;
	    
	   // System.out.println("Month 1 = " + month1Full + " & Month 2 = " + month2Full);
	    
	    char day1Dig1 = dateOne.charAt(3); //This is converting the chars into the int values for the day in input 1
	    int d1D1 = Character.getNumericValue(day1Dig1);
	    char day1Dig2 = dateOne.charAt(4);
	    int d1D2 = Character.getNumericValue(day1Dig2);
	    int day1Full = (d1D1 * 10) + d1D2;
	    
	    char day2Dig1 = dateTwo.charAt(3); //This is converting the chars into the int values for the day in input 2
	    int d2D1 = Character.getNumericValue(day2Dig1);
	    char day2Dig2 = dateTwo.charAt(4);
	    int d2D2 = Character.getNumericValue(day2Dig2);
	    int day2Full = (d2D1 * 10) + d2D2;

	    int greaterDateYear; //A new set of int values to set the years in order past and present (more present)
	    int pastDateYear;
	    	int greaterDateMonth;
	    	int pastDateMonth;
	    	int greaterDateDay;
	    	int pastDateDay;
	    
	    if (year1Full > year2Full) { //This determines which year the more current
	    	greaterDateYear = year1Full;
	    	pastDateYear = year2Full;
	    	greaterDateMonth = month1Full;
	    	pastDateMonth = month2Full;
	    	greaterDateDay = day1Full;
	    	pastDateDay = day2Full;
	    } else {
	    	greaterDateYear = year2Full;
	    	pastDateYear = year1Full;
	    	greaterDateMonth = month2Full;
	    	pastDateMonth = month1Full;
	    	greaterDateDay = day2Full;
	    	pastDateDay = day1Full;
	    }
	    
	    
	    
	    
	    /* This gnarly-looking loop is used to take in consideration the different value of each respective month.
	     * initially the application was much shorter and used absolute values, but absolute values or no absolute values
	     * I did not take into consideration what would happen if the month being subtracted was greater than the month from
	     * the date with the more recent year it would affect the accuracy of the duration*/
		
	    	while (greaterDateDay < pastDateDay) {   
	    		int i;
	    		if (greaterDateMonth == 01) {
	    			i = 31; 
	    			greaterDateDay = (greaterDateDay + i);
		    		greaterDateMonth = (greaterDateMonth -1);
		    		}
	    		if (greaterDateMonth == 02) {
	    			i = 28; 
	    			greaterDateDay = (greaterDateDay + i);
		    		greaterDateMonth = (greaterDateMonth -1);
	    			}
	    		if (greaterDateMonth == 03) {
	    			i = 31; 
	    			greaterDateDay = (greaterDateDay + i);
		    		greaterDateMonth = (greaterDateMonth -1);
	    			}
	    		if (greaterDateMonth == 04) {
	    			i = 30; 
	    			greaterDateDay = (greaterDateDay + i);
		    		greaterDateMonth = (greaterDateMonth -1);
		    		}
	    		if (greaterDateMonth == 05) {
	    			i = 31; 
	    			greaterDateDay = (greaterDateDay + i);
		    		greaterDateMonth = (greaterDateMonth -1);
		    		}
	    		if (greaterDateMonth == 06) {
	    			i = 30; 
	    			greaterDateDay = (greaterDateDay + i);
		    		greaterDateMonth = (greaterDateMonth -1);
		    		}
	    		if (greaterDateMonth == 07) {
	    			i = 31; 
	    			greaterDateDay = (greaterDateDay + i);
		    		greaterDateMonth = (greaterDateMonth -1);
		    		}
	    		if (greaterDateMonth == 8) { //why is 08 and 09 literal type out of range???
	    			i = 31; 
	    			greaterDateDay = (greaterDateDay + i);
		    		greaterDateMonth = (greaterDateMonth -1);
		    		}
	    		if (greaterDateMonth == 9) {
	    			i = 30; 
	    			greaterDateDay = (greaterDateDay + i);
		    		greaterDateMonth = (greaterDateMonth -1);
		    		}
	    		if (greaterDateMonth == 10) {
	    			i = 31; 
	    			greaterDateDay = (greaterDateDay + i);
		    		greaterDateMonth = (greaterDateMonth -1);
		    		}
	    		if (greaterDateMonth == 11) {
	    			i = 30; 
	    			greaterDateDay = (greaterDateDay + i);
		    		greaterDateMonth = (greaterDateMonth -1);}
	    		if (greaterDateMonth == 12) {
	    			i = 31; 
	    			greaterDateDay = (greaterDateDay + i);
		    		greaterDateMonth = (greaterDateMonth -1);
		    		}
	    		else if (greaterDateMonth > 12) {
	    			
	    		}
	    	}
	    	
	    	if (greaterDateMonth < pastDateMonth) { //This allows for the proper calculation of months
	    		greaterDateMonth = greaterDateMonth + 12;
	    		greaterDateYear = greaterDateYear - 1;
	    	}

	    	int yearsRemaining;
	    	int monthsRemaining;
	    	int daysRemaining;
	    	
	    daysRemaining = greaterDateDay - pastDateDay;
	    monthsRemaining = greaterDateMonth - pastDateMonth;
	    yearsRemaining = greaterDateYear - pastDateYear;
	    
	    System.out.println("The duration of time between the two dates is " + yearsRemaining + " years, " + monthsRemaining + " months, and " + daysRemaining + " days.");
	    
	    
}
}
