1. **To create a new database called STUDENTDB**

mysql> CREATE DATABASE STUDENTDB;

Query OK, 1 row affected (0.12 sec)



**2. To display the databases;**

mysql> SHOW DATABASES;

\+	+

| Database	|

\+	+

| information\_schema |

| mysql	|

| performance\_schema |

| studentdb	|

| test	|

\+	+

5 rows in set (0.02 sec)



**3. To use the created database STUDENTDB**

mysql> USE STUDENTDB;

Database changed



**4. Create a table with five columns:**

&nbsp;mysql> CREATE TABLE STUDENT(

-> SNUM INT PRIMARY KEY,

-> SNAME VARCHAR(20) NOT NULL,

-> MAJOR VARCHAR(5) NOT NULL,

-> LEVEL CHAR(5),

-> DOB DATE);

Query OK, 0 rows affected (0.13 sec)



**5. To display/view all the tables in the STUDENTDB database.**

mysql> SHOW TABLES;

\+	+

| Tables\_in\_studentdb |

\+	+

| student	|

\+	+

1 row in set (0.00 sec)



**6.	To display the table description/schema/intension/structure of the database**

mysql> DESC STUDENT;

\+	+	+	+	+	+	+

| Field | Type	| Null | Key | Default | Extra |

\+	+	+	+	+	+	+

| SNUM | int(11)| NO  | PRI | NULL	|	|

| SNAME | varchar(20) | NO  |	| NULL	|	|

| MAJOR | varchar(5) | NO  |	| NULL	|	|

| LEVEL | char(5)	| YES |	| NULL	|	|

| DOB  | date	| YES |	| NULL	|	|

\+	+	+	+	+	+	+



**7. To add a new column called “SEM” to the existing table STUDENT and whose default value is “4”**

mysql> ALTER TABLE STUDENT ADD SEM INT DEFAULT 4;

Query OK, 0 rows affected (0.27 sec) Records: 0 Duplicates: 0 Warnings: 0

mysql> DESC STUDENT;

\+	+	+	+	+	+	+

| Field | Type	| Null | Key | Default | Extra |

\+	+	+	+	+	+	+

| SNUM | int(11)	| NO  | PRI | NULL	|	|

| SNAME | varchar(20) | NO  |	| NULL	|	|

| MAJOR | varchar(5) | NO  |	| NULL	|	|

| LEVEL | char(5)	| YES |	| NULL	|	|

| DOB  | date	| YES |	| NULL	|	|

| SEM  | int(11)	| YES |	| 4	|	|

\+	+	+	+	+	+	+

6 rows in set (0.13 sec)



**8. To modify the definition of a column of the existing table STUDENT**

mysql> ALTER TABLE STUDENT MODIFY MAJOR VARCHAR(20) NULL;

Query OK, 0 rows affected (0.27 sec) Records: 0 Duplicates: 0 Warnings: 0



mysql> DESC STUDENT;

\+	+	+	+	+	+	+

| Field | Type	| Null | Key | Default | Extra |

\+	+	+	+	+	+	+

| SNUM | int(11)	| NO  | PRI | NULL	|	|

| SNAME | varchar(20) | NO  |	| NULL	|	|

| MAJOR | varchar(20) | YES |	| NULL	|	|

| LEVEL | char(5)	| YES |	| NULL	|	|

| DOB  | date	| YES |	| NULL	|	|

| SEM  | int(11)	| YES |	| 4	|	|

\+	+	+	+	+	+	+

6 rows in set (0.03 sec)



**9. To make other column as primary key(unique) in an existing table STUDENT**

mysql> ALTER TABLE STUDENT MODIFY SNAME VARCHAR(20) UNIQUE;

Query OK, 0 rows affected (0.22 sec) Records: 0 Duplicates: 0 Warnings: 0

mysql> DESC STUDENT;

\+	+	+	+	+	+	+

| Field | Type	| Null | Key | Default | Extra |

\+	+	+	+	+	+	+

| SNUM | int(11)	| NO  | PRI | NULL	|	|

| SNAME | varchar(20) | YES | UNIQUE | NULL	|	|

| MAJOR | varchar(20) | YES |	| NULL	|	|

| LEVEL | char(5)	| YES |	| NULL	|	|

| DOB  | date	| YES |	| NULL	|	|

| SEM  | int(11)	| YES |	| 4	|	|

\+	+	+	+	+	+	+





**10. To drop a column in an already created table.**

mysql> ALTER TABLE STUDENT DROP COLUMN LEVEL;

Query OK, 0 rows affected (0.20 sec) Records: 0 Duplicates: 0 Warnings: 0



mysql> DESC STUDENT;

\+	+	+	+	+	+	+

| Field | Type	| Null | Key | Default | Extra |

\+	+	+	+	+	+	+

| SNUM | int(11)	| NO  | PRI | NULL	|	|

| SNAME | varchar(20) | YES | UNI | NULL	|	|

| MAJOR | varchar(20) | YES |	| NULL	|	|

| DOB  | date	| YES |	| NULL	|	|

| SEM  | int(11)	| YES |	| 4	|	|

\+	+	+	+	+	+	+

5 rows in set (0.03 sec)



**11. Truncating the tables. Syntax:**

Truncate table <tablename>;

mysql> TRUNCATE TABLE ENROLL1;

Query OK, 0 rows affected (0.11 sec)





**12. To delete the definition/schema/description/structure of a table.** 

&nbsp;	Syntax:

Drop table <tablename>;

Example:

mysql> DROP TABLE ENROLL1;

Query OK, 0 rows affected (0.08 sec)













