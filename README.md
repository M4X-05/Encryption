# Encryption

package com.company;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
	//Import scanner for user input
	Scanner scan = new Scanner(System.in);
	//Welcome question for the user to decide if they want something Encrypted, "1", or Decrypted, "2".
	System.out.println("Hello, Welcome to The Maxwell Encryption Agency. To Encrypt a word insert 1 to Decrypt a word insert 2");
	//Scanning for user input which is either 1 or 2
	String userInput = scan.next();

	//if statement when the user inputs 1 - to encrypt a word
	if(userInput.equals("1")) {
		//Asks the user what word they want encrypted
		System.out.println("Please insert the word you would like Encrypted");
		//Scanning for the user's word
		String userWord = scan.next();
		//This figures out the last letter in the word - step 1 of the encryption
		String lastLetter = userWord.substring(userWord.length()-1);
		//This figures out what part of the word is remaining - step 2 of the encryption
		String remainingWord = userWord.substring(0, userWord.length()-1);
		//This builds the encrypted word: last letter + remaining part of the word + "ay" - step 3 of the encryption
		String wordEncrypt = lastLetter + remainingWord + "ay";
		//Displays the encrypted word
		System.out.println("Your Encrypted word is:\t" + wordEncrypt);
		//Goodbye statement
		System.out.println("Thanks For visiting The Maxwell Encryption Agency!");
	}
	//if statement when the user inputs 2 - to decrypt a word
	if(userInput.equals("2")) {
		//Asks the user what word they want decrypted
		System.out.println("Please insert the word you would like Decrypted");
		//Scanning for the user's word
		String userWord = scan.next();
		//This figures out the first letter in the word - step 1 of the decryption
		String firstLetter = userWord.substring(0,1);
		//This figures out the remaining letters in the word minus the "ay" at the end - step 2 of the decryption
		String remainingWord = userWord.substring(1, userWord.length()-2);
		//This builds the decrypted word: remaining part of the word + the first letter - step 3 of the decryption
		String wordDecrypted = remainingWord + firstLetter;
		//Displays the decrypted word
		System.out.println("Your Decrypted word is:\t" + wordDecrypted);
		//Goodbye statement
		System.out.println("Thanks For visiting The Maxwell Encryption Agency!");
	}
	}
}
