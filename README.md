📚 Library Management System (DBMS Project)

This project implements a Library Management System using SQL & PL/SQL.
It is designed to manage customers, employees, books, videos, branches, and rental transactions while ensuring data integrity with relational constraints and stored procedures.

📂 Project Structure

LIBRARY PROJECT.sql → Contains table creation, constraints, inserts, and PL/SQL procedures/functions.

plsql.pdf → Detailed project report with introduction, requirements, ER diagram, normalization, schema, and explanation of functionalities.

ER_model.jpg → ER diagram of the system.

🛠 Features

Customer & Employee Management

Secure login system with credentials.

Employee details including paycheck and branch information.

Card System

Each customer/employee is assigned a library card.

Tracks fines, status (active/blocked).

Book & Video Management

Maintains inventory of books (ISBN, state, availability, costs).

Maintains videos (title, year, state, costs).

Branch & Location Handling

Each branch has an address, phone, and location.

Rental System

Rent books/videos using library cards.

Automatic updates of item availability.

Maintains appropriation date and return date.

Fine Management

Customers can pay fines.

System updates card status after payment.

PL/SQL Functionalities

Login validation (loginCustomer_library, loginEmployee_library).

View item details (viewItem_library).

Rent an item (rentItem_library).

Pay fines (payFines_library).

List all books/videos (allMedia_library using cursors).

🗃️ Database Schema (Simplified)

Tables:

CARD (cardID, status, fines)

CUSTOMER (customerID, name, address, phone, username, password, dateSignUp, cardNumber)

EMPLOYEE (employeeID, name, address, phone, username, password, paycheck, branchName, cardNumber)

BRANCH (name, address, phone)

LOCATION (address)

BOOK (ISBN, itemID, state, availability, debyCost, lostCost, address)

VIDEO (title, year, itemID, state, availability, debyCost, lostCost, address)

RENT (cardID, itemID, appropriationDate, returnDate)

📊 ER Diagram

🚀 How to Run

Install Oracle SQL/PLSQL or any compatible database system.

Import and execute the SQL file:

@LIBRARY PROJECT.sql


Run the procedures/functions to test functionalities.

📖 Documentation

Full project documentation is available in plsql.pdf
, which covers:

Introduction & Requirements

ER Diagram

Normalization

Schema & Constraints

Stored Procedures

Cursors
