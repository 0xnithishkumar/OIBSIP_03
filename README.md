# Explanation of code:- 

=> This is a Java program that simulates a basic banking application. It has several functions that allow the user to perform various actions such as checking their transaction history, withdrawing money, depositing money, transferring money, and quitting the application. The program uses a Scanner object to read input from the command line and an ArrayList to store a list of transactions.

=> The transac function is used to display the transaction history to the user. The login function checks if the user's username and pin are valid, and if they are, the user is logged in and the ask function is called with an initial balance of 10000. If the login information is invalid, the user is prompted to enter valid information.

=> The withdraw, deposit, and transfer functions are used to allow the user to perform the corresponding actions with their account. These functions all check if the amount entered by the user is valid (i.e. greater than or equal to 0 and less than or equal to the current balance for withdraw and transfer, and greater than or equal to 0 for deposit) and if it is, the balance is updated and the transaction is recorded in the list of transactions. If the amount is invalid, the user is prompted to enter a valid amount.

=> The quit function allows the user to exit the application by entering 'y' or 'Y'. If any other character is entered, the program returns to the ask function where the user can choose another action. The ask function presents the user with a list of actions and prompts them to choose one. If an invalid option is chosen, the user is prompted to enter a valid input.



# How to use:-

=> This will start the program and prompt you to enter your username and pin. If you enter a valid username (i.e. "test") and pin (i.e. 0000), you will be logged in and presented with a list of actions to choose from. You can then choose one of the actions by entering the corresponding number. For example, if you want to check your transaction history, you can enter "1". If you want to withdraw money, you can enter "2", and so on.

=> You can use the program to perform various actions such as checking your transaction history, withdrawing money, depositing money, transferring money to another account, or quitting the application. The program will prompt you for any additional information that is needed for each action. Once you have completed all the actions that you want to perform, you can quit the program by entering "5" and then entering 'y' or 'Y' when prompted.



# Psuesocode:- 
      import java.util.Scanner
      import java.util.ArrayList

      class Main {

          // Initialize Scanner object and ArrayList
          public static Scanner sc = new Scanner(System.in)
          public static ArrayList<String> list = new ArrayList<>()

          // Display transaction history to user
          public static void transac(int balance) {
              for (String i : list) {
                  print(i)
              }
              ask(balance)
          }

          // Check if login information is valid
          public static void login(String username, int pin) {
              if (username.contains("test") && pin == 0000) {
                  list.add("Logged in")
                  ask(10000)
              } else {
                  print("Enter valid info!")
                  print("Username followed by pin seperated with a space: ")
                  login(sc.next(), sc.nextInt())
              }
          }

          // Withdraw money from account
          public static void withdraw(int balance, int amount) {
              if (amount <= balance && amount >= 0) {
                  balance -= amount
                  print("Transaction successful, Current balance is " + balance)
                  list.add("Rupee/'s " + amount + " withdrawn.")
                  ask(balance)
              } else {
                  print("Enter a valid amount(greater than equal to 0): ")
                  withdraw(balance, sc.nextInt())
              }
          }

          // Deposit money into account
          public static void deposit(int balance, int amount) {
              if (amount >= 0) {
                  balance += amount
                  print("Transaction successful, Current balance is " + balance)
                  list.add(amount + " ruppee/'s deposited!")
                  ask(balance)
              } else {
                  print("Enter a valid amount(greater than equal to 0): ")
                  deposit(balance, sc.nextInt())
