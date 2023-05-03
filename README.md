Download Link: https://assignmentchef.com/product/solved-cs1301-lab-07-fun-with-strings
<br>
Good programmers think before they begin coding. Part I of this assignment involves brainstorming with a group of peers with no computers to talk about a strategy for solving this week’s lab. Breakup into groups based on your seating (3-4 people per group) and brainstorm about how to solve the problems below. Make sure everyone understands the problem and sketch out potential ways to move toward a solution.  You may find it helpful to look over the required readings for this week.

<strong>Note: Brainstorms are to help you get started with the lab and get you in the habit of designing before you code.  You won’t submit them to eLC. </strong>

<h1>Prerequisites</h1>

The lab deals mainly with material from Chapter 4 (loops and nested loops) but builds on material learned in Chapters 2-3 – especially the material on Strings.

<h1>Lab Details</h1>

In this lab, you will create an environment where the user can enter a sentence (as a string) and then manipulate that string using 5 basic commands. These manipulations will affect the successive commands that they make. Look at the output examples for a clear demonstration of this. You will implement these commands using loops and basic string methods.  You are NOT permitted to use the StringBuilder class, Arrays class, or any class in java.util.stream (the use of any of these will result in a grade of zero on this assignment).  Furthermore, do not use any break or continue statements in the body of your loops.

<strong>The ONLY String methods that you can use for this lab are:  </strong>

<strong>length, concat, +, charAt, substring, and equals (or equalsIgnoreCase). </strong>

When the program begins, it asks the user to input a String.  This input can range from a single letter to a complete sentence.




The program will then list the 6 possible commands that the user can choose from (see below). The user can use these commands to modify the original sentence. The program will continue to ask for commands until the user enters the “quit” command.  The 6 commands are:




<ul>

 <li><strong>Reverse</strong>: If the user types “reverse” with any capitalization, your program will reverse the original string and print the result.</li>

 <li><strong>Replace First</strong>: If the user types “replace first” with any capitalization, your program will prompt the user to enter the character to replace and the new character (to replace the old character). Afterwards, it will replace the <u>first</u> instance of the old character with the new character (see example output below) and prints the modified string.</li>

 <li><strong>Replace Last</strong>: If the user types “replace last” with any capitalization, your program will prompt the user to enter the character to replace and the new character (to replace the old character). Afterwards, it will replace the <u>last</u> instance of the old character with the new character (see example output below) and prints the modified string.</li>

 <li><strong>Remove</strong>: If the user types “remove” with any capitalization, your program will prompt the user to enter the character to remove, and which instance it should remove (it can remove any instance of the character). The program will then carry out the remove and print the modified string.</li>

 <li><strong>Remove All: </strong>If the user types “remove all”, with any capitalization, your program will prompt the user to enter the character to remove. Then, it removes all instances of the given letter in the sentence.  This command also prints the modified sentence to the console.</li>

 <li><strong>Quit</strong>: stops the program.</li>

</ul>

<strong> </strong>

<h1>Error Handling</h1>

The program should print a friendly error message and continue to the next command if any of the following arises:

<ul>

 <li>The user tries to replace or remove a character not in the input string</li>

 <li>The user tries to remove the 3<sup>rd</sup> ‘a’ from the sentence but there is no 3<sup>rd</sup> ‘a’</li>

 <li>There may be additional error situations that you can catch and handle gracefully. You should make every attempt to handle these situations when possible.  If you are unsure if you need to handle a particular error, post a question to Piazza.</li>

</ul>

In all commands above, when the user enters a character, you should assume that <strong>case matters</strong>.  For example, if the user says remove all ‘A’ characters, your program should not remove ‘a’ characters. Also, the user may enter numbers and special characters and they can be treated as any other character. In other words, no need to modify your code specifically to handle these values.

<h1>Hints</h1>

<ul>

 <li>You have multiple days to complete this lab. Start by writing one command, convince yourself that it is working perfectly, then move onto the next command. Don’t try to do all six at one time.</li>

 <li>While this lab will require nested loops, <strong>you should NOT start by trying to write nested loops</strong>. Practice and review the textbook material about nested loops before attempting to nest your loops. Only after you are fully convinced that all six of the commands are all working should you proceed to wrap your program in a loop to make them execute multiple times.</li>

 <li>Store your user’s string in a variable and modify that variable with every command. If you are simply printing the correct value after the user enters a command but not modifying a variable, you will not have the updated value on the next loop iteration.</li>

</ul>




<h1>Sample Input and Output</h1>

Notice that in these examples manipulations of the input string are carried forward to successive commands.




<strong>Example 1: Testing Reverse </strong>

Enter the string to be manipulated

Go Dawgs

Enter your command (reverse, replace first, replace last, remove all, remove, quit) reverse

The new sentence is: sgwaD oG

Enter your command (reverse, replace first, replace last, remove all, remove, quit) reverse

The new sentence is: Go Dawgs

Enter your command (reverse, replace first, replace last, remove all, remove, quit)

Quit

<strong>…Execution Ends… </strong>

<strong> </strong>

<strong>Example 2: Testing replace first and last and capitalization of commands </strong>

Enter the string to be manipulated

Co Dawcs

Enter your command (reverse, replace first, replace last, remove all, remove, quit)

RePlAcE FiRST

Enter the character to replace

C

Enter the new character

G

The new sentence is: Go Dawcs

Enter your command (reverse, replace first, replace last, remove all, remove, quit) replace LAST

Enter the character to replace c

Enter the new character g

The new sentence is: Go Dawgs

Enter your command (reverse, replace first, replace last, remove all, remove, quit)

Quit

<strong>…Execution Ends… </strong>

<strong> </strong>

<strong>Example 3: Letter not found with replace first </strong>




Enter the string to be manipulated

co dawcs

Enter your command (reverse, replace first, replace last, remove all, remove, quit) replace FIRST

Enter the character to replace

C

Enter the new character

G

The letter was not found in the word

Enter your command (reverse, replace first, replace last, remove all, remove, quit) replace first

Enter the character to replace c

Enter the new character

G

The new sentence is: Go dawcs

Enter your command (reverse, replace first, replace last, remove all, remove, quit)

Quit

<strong>…Execution Ends… </strong>

<strong> </strong>

<strong>Example 4: Testing remove and remove all </strong>Enter the string to be manipulated cazzzzooooo dawggggooooos

Enter your command (reverse, replace first, replace last, remove all, remove, quit) remove ALL

Enter the character to remove o

The new sentence is: cazzzz dawggggs

Enter your command (reverse, replace first, replace last, remove all, remove, quit) remove

Enter the character to remove z

Enter the z you would like to remove (Not the index – 1 = 1st, 2 = 2nd, etc.):

4

The new sentence is: cazzz dawggggs

Enter your command (reverse, replace first, replace last, remove all, remove, quit) remove

Enter the character to remove g

Enter the g you would like to remove (Not the index – 1 = 1st, 2 = 2nd, etc.):

4

The new sentence is: cazzz dawgggs

Enter your command (reverse, replace first, replace last, remove all, remove, quit) remove

Enter the character to remove g

Enter the g you would like to remove (Not the index – 1 = 1st, 2 = 2nd, etc.):

5

Error: the letter you are trying to remove does not exist

Enter your command (reverse, replace first, replace last, remove all, remove, quit) remove

Enter the character to remove a

Enter the a you would like to remove (Not the index – 1 = 1st, 2 = 2nd, etc.):

1

The new sentence is: czzz dawgggs

Enter your command (reverse, replace first, replace last, remove all, remove, quit) remove all

Enter the character to remove z

The new sentence is: c dawgggs

Enter your command (reverse, replace first, replace last, remove all, remove, quit) remove all

Enter the character to remove c

The new sentence is:  dawgggs

Enter your command (reverse, replace first, replace last, remove all, remove, quit) Quit

<strong>…Execution Ends… </strong>

<strong> </strong>

<strong> </strong>