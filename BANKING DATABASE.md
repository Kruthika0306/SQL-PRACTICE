 **BANKING DATABASE**



CREATE DATABASE BANKINGDB;

USE BANKINGDB;



CREATE TABLE CUSTOMER (

&nbsp;CustomerID INT PRIMARY KEY,

&nbsp;CustomerName VARCHAR(50) NOT NULL,

&nbsp;Email VARCHAR(50) UNIQUE,

&nbsp;Phone VARCHAR(15) UNIQUE

);



CREATE TABLE ACCOUNT (

&nbsp;AccountNo INT PRIMARY KEY,

&nbsp;CustomerID INT,

&nbsp;AccountType VARCHAR(20) NOT NULL,

&nbsp;Balance DECIMAL(10,2) NOT NULL,

&nbsp;FOREIGN KEY (CustomerID) REFERENCES CUSTOMER(CustomerID)

);



CREATE TABLE TRANSACTION\_DETAILS (

&nbsp;TransactionID INT PRIMARY KEY,

&nbsp;AccountNo INT,

&nbsp;Amount DECIMAL(10,2) NOT NULL,

&nbsp;TransactionType VARCHAR(20),

&nbsp;FOREIGN KEY (AccountNo) REFERENCES ACCOUNT(AccountNo)

);



INSERT INTO CUSTOMER VALUES

(1,'Ravi','ravi@gmail.com','9876543210'),

(2,'Anita','anita@gmail.com','9123456780');



INSERT INTO ACCOUNT VALUES

(101,1,'Savings',50000),

(102,2,'Current',75000);



INSERT INTO TRANSACTION\_DETAILS VALUES

(1001,101,5000,'Deposit'),

(1002,102,3000,'Withdrawal');





