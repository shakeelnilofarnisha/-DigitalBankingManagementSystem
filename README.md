# 🏦 Digital Banking Management System

### A Java-Based Banking Application using SQLite and JDBC

![Java](https://img.shields.io/badge/Java-17%2B-orange)
![Database](https://img.shields.io/badge/Database-SQLite-blue)
![Connectivity](https://img.shields.io/badge/Connectivity-JDBC-green)
![Project](https://img.shields.io/badge/Project-Academic-purple)

---

## 📌 Project Overview

The **Digital Banking Management System** is a Java console-based application developed using Object-Oriented Programming concepts, SQLite and JDBC.

It provides basic banking operations for customers and administrators, including account management, deposits, withdrawals, fund transfers and transaction history.

## ✨ Features

### 👤 Customer Features
- Customer Registration and Login
- Open Savings and Current Accounts
- View Bank Accounts
- Deposit Money
- Withdraw Money
- Transfer Money Between Accounts
- View Transaction History
- Calculate Savings Interest

### 🔐 Admin Features
- Administrator Account Setup
- Admin Login
- View and Search Accounts
- Freeze and Activate Accounts
- View Customer Details
- Account and Transaction Statistics

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Java | Application Development |
| SQLite | Database Management |
| JDBC | Database Connectivity |
| SQL | Database Operations |
| OOP | Application Structure |

## 🧠 OOP Concepts Implemented

- **Encapsulation:** Private fields and controlled access through methods.
- **Abstraction:** Abstract BankAccount class.
- **Inheritance:** SavingsAccount and CurrentAccount extend BankAccount.
- **Polymorphism:** Different withdrawal and interest calculation implementations.

## 📂 Project Structure

```text
DigitalBankingManagementSystem/
│
├── DigitalBankingSystem.java
├── schema.sql
├── README.md
├── run.bat
├── sqlite-jdbc.jar
└── digital_banking.db
```

## ⚙️ Requirements

- Java JDK 17 or later
- Windows Operating System (for run.bat)
- SQLite JDBC Driver

No separate SQLite installation is required.

## 🚀 How to Run

1. Download or clone this repository.
2. Extract the project folder.
3. Make sure Java JDK 17 or later is installed.
4. Double-click `run.bat`.
5. Create the administrator account on the first run.
6. Start using the banking application.

### Run Using Command Prompt

```bash
javac -d . DigitalBankingSystem.java
java --enable-native-access=ALL-UNNAMED -cp ".;sqlite-jdbc.jar" bank.banking.DigitalBankingSystem
```

## 🗄️ Database

The application uses SQLite for storing:

- Customer Information
- Administrator Information
- Bank Account Details
- Transaction Records

The database is automatically created when the application runs.

## 🔒 Security

- Passwords are salted and hashed using PBKDF2-HMAC-SHA256.
- Prepared statements are used for database operations.
- Database transactions help maintain data consistency.

## 📌 Important Note

This is an educational project developed for academic purposes. It uses local SQLite storage and simulated balances. It does not connect to real banks or process real payments.

---

## 👩‍💻 Project

**Digital Banking Management System**

Developed using Java, SQLite and JDBC.
