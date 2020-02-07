# Assignment - Create a Test Plan

Your task is to create and execute a test plan for the game Coffee Maker Quest, based on the requirements listed below. There are several defects in the software; you will need to find and report on at least three. Additionally, you must create a *traceability matrix* showing the mapping of test cases to requirements.  

There should be at least as many test cases as requirements. A general rule of thumb is that if you have *less* than 2x as many test cases as requirements, you're probably doing too little, but if you have *more* than 4x as many test cases as requirements, consider whether you are over-testing. Remember that every requirement has at least one "happy case", and probably one or more "sad cases" also.

Each requirement should have AT LEAST one test case associated with it, and each test should have EXACTLY ONE requirement associated with it. This can easily be checked via a traceability matrix, which you should also deliver. If you don't like the format in the book, you can use e.g. the table format shown in https://en.wikipedia.org/wiki/Traceability_matrix  

Test cases should mention all necessary preconditions, input values, execution steps, output values, and postconditions.  

You'll probably find the defects by exploratory testing. However, you should also execute your test plan to confirm that it finds the defects you've identified. 

## Your Report

You should submit a PDF file containing your report.

The structure of the file should be as follows:
 - Document title "Coffee Maker Quest Test Plan"
 - Section titled "Introduction" 
   - Here you can note any concerns or difficulties you may have had or anticipate with the testing process. You could also note why you considered certain test cases, how you thought of edge cases, etc.  
 - Section titled "Requirements"
   - Copy the Requirements section below
 - Section titled "Test Cases"
   - Include all the test cases. You may name or number them any way you wish, but be consistent. Use the format from the lecture or textbook, i.e. Identifier, Description, Preconditions, Input Values, Execution Steps, Output Values, Postconditions (all on separate lines)
 - Section titled "Traceability Matrix"
    - Include a traceability matrix which maps the test cases and their associated requirements. Remember that all requirements should map to AT LEAST ONE test case, and all test cases should map to EXACTLY ONE requirement.  
 - Section titled "Defects Found"
    - List at least three defects found. The defects should follow the following defect reporting style: Identifier, Description, Reproduction Steps, Expected Behavior, Observed Behavior (all on separate lines)
 - Section titled "Who Did What"
    - List all members of the team, and what roles they played in the project

## Tips for the Test Plan

Be as precise as possible in your descrptions. Don't say "Ensure that you see the correct value"; say that "You should see the text 'A Smart door leads South'". Don't say "go north"; say "Type n ".  

Remember to write down all the necessary steps and preconditions!  

The "Description" of a test cases should be a one-sentence description of the test case in plain English. For example, "Ensure that user can go North from the starting room."  

You should not need to exhaustively test the application. If you find yourself with more than four test cases per requirement, you may be over-testing. This is admirable in software where human life is at stake, but this is only your grade. 

This is a test plan, not a test run - remember the difference.  

Note that if you find yourself in a magical land - even if you get transported back to where you came from - you may have gone through a door which did not exist. Think about if that meets the requirements or not.  

Remember that tests should be reproducible - starting with all preconditions met, anybody should be able to reproduce the same steps and get the same results. If they can't, rethink your preconditions!  

## Coffee Maker Quest

Coffee Maker Quest is a simple game. The goal is to get coffee, sugar, and cream, and then drink it so that you can stay up and study. In order to do so, you need to visit several rooms in a house and look around. Once you have obtained all the necessary elements, you win. If you decide to drink before getting all of the necessary elements, you lose.  

Given an installed copy of Java, you can run the game using the associated coffeemaker.jar file:

```bash
java -jar coffeemaker.jar
```

## Requirements

- FUN-ITERATION - At each iteration of the game, the user shall be able enter one of six commands - "N" to go North, "S" to go South, "L" to Look for items, "I" for Inventory, "H" for Help, or "D" to Drink.
- FUN-UNKNOWN-COMMAND - If a player enters a command not specified by FUN-ITERATION, the system shall respond with the phrase "What?".
- FUN-INPUT-CAPS - The system shall be case-insensitive in regards to input values; that is, it shall accept capital and lower-case letters and treat them as equivalent.
- FUN-MOVE - The system shall allow a player to move North only if a door exists going North, and South only if a door exists going South.
- FUN-WIN - The player shall win the game if and only if Coffee, Sugar, and Cream have been collected by the player and then drunk.
- FUN-LOSE - The player shall lose the game if and only if the player Drinks but has not collected all of the items (Coffee, Sugar, and Cream).
- FUN-INVENTORY - Upon entering "I" for inventory, the player shall be informed of the items that he/she has collected (consisting of Coffee, Sugar, and Cream).
- FUN-LOOK - Upon entering "L" for Look, the player shall collect any items in the room and those items will be added to the player's inventory.
- FUN-HELP - Upon entering "H" for Help, the player shall be shown a listing of possible commands and what their effects are.
- FUN-UNIQ-ROOM - Each room in the house shall have a unique adjective describing it.
- FUN-UNIQ-ROOM-FURNISHING - Each room in the house shall have one and only one unique furnishing visible to the user upon entering the room.

