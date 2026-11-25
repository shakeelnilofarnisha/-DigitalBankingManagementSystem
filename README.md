DIGITAL BANKING MANAGEMENT SYSTEM
Java console application with SQLite and JDBC

FILES
  DigitalBankingSystem.java  Application source
  schema.sql                 Database schema
  run.bat                    Compile and launch on Windows
  sqlite-jdbc.jar            SQLite JDBC driver

REQUIREMENTS
  Java JDK 17 or newer
  Windows for run.bat; on another OS, use the commands below with the correct classpath separator.
  No separate SQLite installation is required. The database is created automatically.

RUN ON WINDOWS
  1. Extract the ZIP file.
  2. Double-click run.bat, or open Command Prompt in the extracted folder.
  3. Run:
       javac -d . DigitalBankingSystem.java
       java --enable-native-access=ALL-UNNAMED -cp ".;sqlite-jdbc.jar" bank.banking.DigitalBankingSystem

FIRST RUN
  Create an administrator username, full name, email, and password when prompted.
  Customer accounts are created after customer registration and login.
  The application creates digital_banking.db automatically in the current folder.

FEATURES
  Customers: registration/login, open savings/current accounts, view accounts, deposits,
             withdrawals, transfers between accounts, transaction history, savings interest.
  Admin:     first-run admin setup, login, list/search accounts, freeze/activate accounts,
             customer listing, account and transaction statistics.
  Rules:     savings accounts earn 4% interest and maintain a minimum $500 balance;
             current accounts earn no interest and maintain a minimum $1000 balance.
  Security:  passwords are salted and hashed with PBKDF2-HMAC-SHA256; database writes use
             prepared statements and transactions.

OOP CONCEPTS
  Encapsulation: account/customer records are managed through controlled methods and private fields.
  Abstraction:   abstract BankAccount plus SavingsAccount and CurrentAccount implementations.
  Inheritance:   SavingsAccount and CurrentAccount extend BankAccount.
  Polymorphism:  account-specific withdraw and calculateInterest implementations.

NOTES
  This is an educational project, not a production banking system. It uses local SQLite storage
  and simulated balances; it does not connect to real banks or process real payments.
