 CREATE DATABASE LibraryDB;
Query OK, 1 row affected (0.01 sec)

mysql> USE LibraryDB;
Database changed
mysql> CREATE TABLE Authors (
    ->     AuthorID INT PRIMARY KEY AUTO_INCREMENT,
    ->     Name VARCHAR(100),
    ->     Bio TEXT
    -> );
Query OK, 0 rows affected (0.04 sec)

mysql> CREATE TABLE Categories (
    ->     CategoryID INT PRIMARY KEY AUTO_INCREMENT,
    ->     CategoryName VARCHAR(100)
    -> );
Query OK, 0 rows affected (0.04 sec)

mysql> CREATE TABLE Books (
    ->     BookID INT PRIMARY KEY AUTO_INCREMENT,
    ->     Title VARCHAR(200),
    ->     AuthorID INT,
    ->     CategoryID INT,
    ->     ISBN VARCHAR(20) UNIQUE,
    ->     PublishedYear YEAR,
    ->     FOREIGN KEY (AuthorID) REFERENCES Authors(AuthorID),
    ->     FOREIGN KEY (CategoryID) REFERENCES Categories(CategoryID)
    -> );
Query OK, 0 rows affected (0.06 sec)

mysql> CREATE TABLE Members (
    ->     MemberID INT PRIMARY KEY AUTO_INCREMENT,
    ->     FullName VARCHAR(100),
    ->     Email VARCHAR(100) UNIQUE,
    ->     JoinDate DATE
    -> );
Query OK, 0 rows affected (0.04 sec)

mysql> CREATE TABLE Loans (
    ->     LoanID INT PRIMARY KEY AUTO_INCREMENT,
    ->     BookID INT,
    ->     MemberID INT,
    ->     IssueDate DATE,
    ->     ReturnDate DATE,
    ->     FOREIGN KEY (BookID) REFERENCES Books(BookID),
    ->     FOREIGN KEY (MemberID) REFERENCES Members(MemberID)
    -> );
Query OK, 0 rows affected (0.06 sec)

mysql> show tables;
+---------------------+
| Tables_in_librarydb |
+---------------------+
| authors             |
| books               |
| categories          |
| loans               |
| members             |
+---------------------+
5 rows in set (0.01 sec)
