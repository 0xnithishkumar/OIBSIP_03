# Explanation of code:- 

- This is a Java program that simulates a basic banking application. It has several functions that allow the user to perform various actions such as checking their transaction history, withdrawing money, depositing money, transferring money, and quitting the application. The program uses a Scanner object to read input from the command line and an ArrayList to store a list of transactions.

- The transac function is used to display the transaction history to the user. The login function checks if the user's username and pin are valid, and if they are, the user is logged in and the ask function is called with an initial balance of 10000. If the login information is invalid, the user is prompted to enter valid information.

- The withdraw, deposit, and transfer functions are used to allow the user to perform the corresponding actions with their account. These functions all check if the amount entered by the user is valid (i.e. greater than or equal to 0 and less than or equal to the current balance for withdraw and transfer, and greater than or equal to 0 for deposit) and if it is, the balance is updated and the transaction is recorded in the list of transactions. If the amount is invalid, the user is prompted to enter a valid amount.

- The quit function allows the user to exit the application by entering 'y' or 'Y'. If any other character is entered, the program returns to the ask function where the user can choose another action. The ask function presents the user with a list of actions and prompts them to choose one. If an invalid option is chosen, the user is prompted to enter a valid input.



# How to use:-

- This will start the program and prompt you to enter your username and pin. If you enter a valid username (i.e. "test") and pin (i.e. 0000), you will be logged in and presented with a list of actions to choose from. You can then choose one of the actions by entering the corresponding number. For example, if you want to check your transaction history, you can enter "1". If you want to withdraw money, you can enter "2", and so on.

- You can use the program to perform various actions such as checking your transaction history, withdrawing money, depositing money, transferring money to another account, or quitting the application. The program will prompt you for any additional information that is needed for each action. Once you have completed all the actions that you want to perform, you can quit the program by entering "5" and then entering 'y' or 'Y' when prompted.



# Psuesocode:- 
- Import the Scanner and ArrayList classes from the java.util package.
- Declare a static Scanner object and an ArrayList of strings.
- Create a "transac" function that displays the transaction history and calls the "ask" function.
- Create a "login" function that checks if the given username and pin are valid. If they are, add a log message to the ArrayList and call the "ask" function. If they are not, ask the user to enter valid information.
- Create a "withdraw" function that allows the user to withdraw a specified amount from their account. If the amount is valid, update the balance and add a log message to the ArrayList. Otherwise, ask the user to enter a valid amount.
- Create a "deposit" function that allows the user to deposit a specified amount into their account. If the amount is valid, update the balance and add a log message to the ArrayList. Otherwise, ask the user to enter a valid amount.
- Create a "transfer" function that allows the user to transfer a specified amount to another user's account. If the amount is valid, update the balance, add a log message to the ArrayList, and ask the user to enter the recipient's username. Otherwise, ask the user to enter a valid amount.
- Create a "quit" function that allows the user to exit the program.
- Create an "ask" function that presents the user with a list of options and allows them to choose one of the actions. If the user's choice is invalid, ask them to enter a valid input. If the user's choice is valid, execute the corresponding function.
- In the main function, ask the user for their username and pin, and call the "login" function.
