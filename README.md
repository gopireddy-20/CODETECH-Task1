# CODETECH-Task1
NAME:
COMPANY:
ID:
DOMAIN:
DURATION:
MENTOR:
#overview of the project
Certainly! Here’s an overview of the Java banking system project:

### **Project Overview**

### **Project: Exploratory Java Programming On Online Banking System**
#### **Objective**
The project is a console-based online banking system implemented in Java. It allows users to perform various banking operations such as creating accounts, depositing and withdrawing funds, transferring money between accounts, viewing transaction history, and managing personal information.

#### **Key Components**
1. **Account Class**: Represents a bank account with methods to handle transactions and maintain transaction history.
2. **User Class**: Represents a bank user with methods for managing accounts and authenticating user credentials.
3. **BankingSystem Class**: Manages the overall application flow, user interactions, and operations related to banking and user management.

#### **Functionality**

1. **User Management**
   - **Register**: Users can register by providing a username and password. Existing usernames are not allowed.
   - **Login**: Registered users can log in with their credentials. Only valid users can access their accounts.

2. **Account Management**
   - **Create Account**: After logging in, users can create new bank accounts with unique account numbers.
   - **Deposit Funds**: Users can deposit funds into their accounts.
   - **Withdraw Funds**: Users can withdraw funds from their accounts, provided they have sufficient balance.
   - **Transfer Funds**: Users can transfer money from one account to another within their profile.

3. **Transaction History**
   - **View History**: Users can view the transaction history of their accounts, which includes deposits, withdrawals, and transfers.

4. **Personal Information Management**
   - **Change Password**: Users can update their account password.
   - **Logout**: Users can log out from their current session.

#### **Classes and Their Responsibilities**

1. **Account Class**
   - **Attributes**: 
     - `accountNumber`: Unique identifier for the account.
     - `balance`: Current balance of the account.
     - `transactionHistory`: List of all transactions performed on the account.
   - **Methods**: 
     - `deposit(double amount)`: Adds funds to the account and records the transaction.
     - `withdraw(double amount)`: Removes funds from the account if sufficient balance exists and records the transaction.
     - `transfer(Account targetAccount, double amount)`: Transfers funds between accounts and updates transaction history.

2. **User Class**
   - **Attributes**: 
     - `username`: User’s login name.
     - `password`: User’s login password.
     - `accounts`: List of accounts owned by the user.
   - **Methods**: 
     - `addAccount(Account account)`: Adds a new account to the user’s list of accounts.
     - `getAccount(String accountNumber)`: Retrieves an account by its number.
     - `validatePassword(String password)`: Checks if the provided password matches the user’s password.

3. **BankingSystem Class**
   - **Attributes**: 
     - `users`: A map storing all registered users with their usernames as keys.
     - `scanner`: Used for user input.
   - **Methods**: 
     - `registerUser()`: Handles user registration.
     - `loginUser()`: Manages user login and returns a `User` object upon successful authentication.
     - `createAccount(User user)`: Allows users to create new accounts.
     - `deposit(User user)`: Handles deposits into the user's account.
     - `withdraw(User user)`: Manages withdrawals from the user's account.
     - `transfer(User user)`: Facilitates fund transfers between accounts.
     - `viewTransactionHistory(User user)`: Displays transaction history for an account.
     - `managePersonalInfo(User user)`: Allows users to change their password or log out.
     - `start()`: Main loop for the application, handling user input and directing flow based on user choices.

#### **Project Execution**

1. **Initialization**: When the program starts, the user is presented with options to either register, log in, or exit.
2. **User Interaction**: After logging in, users can create and manage accounts, perform transactions, and view transaction histories.
3. **Application Flow**: The `start()` method controls the flow of the application, repeatedly prompting the user for actions and executing the corresponding methods.

#### **Technical Details**

- **Input Handling**: Uses `Scanner` for reading user inputs.
- **Transaction Management**: Transactions are recorded in the account’s transaction history list.
- **Data Storage**: User data and accounts are stored in memory using Java collections (`HashMap` and `ArrayList`). Persistent storage (e.g., databases) is not implemented.

#### **Limitations**

- **Security**: No encryption or hashing for passwords. In a real-world scenario, passwords should be securely hashed and stored.
- **Persistence**: Data is not saved between program runs. Adding persistent storage would require database integration.
- **Error Handling**: Basic error messages are provided, but more robust error handling and validation could be implemented.

This project provides a foundational understanding of how a simple banking system can be built in Java and can be expanded upon for more advanced features and security measures.
