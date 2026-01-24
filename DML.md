**Updating the contents of a table.**



**i) updating all rows**



**Syntax**: Update <tablename> set <col>=<exp>,<col>=<exp>;

Before updating the snapshot of Student Table 

mysql> SELECT \* FROM STUDENT;

\+	+	+	+	+	+

| SNUM | SNAME	| MAJOR | DOB	| SEM |

\+	+	+	+	+	+

| 1001 | CHETHAN	| CSE  | 2000-11-03 |	4 |

| 1002 | CHETHAN CHAVAN | CSE  | 2000-11-03 |	4 |

\+	+	+	+	+	+

2 rows in set (0.00 sec)



mysql> UPDATE STUDENT SET MAJOR='ISE';

Query OK, 2 rows affected (0.07 sec) Rows matched: 2 Changed: 2 Warnings: 0

After updating the snapshot of Student Table 

mysql> SELECT \* FROM STUDENT;

\+	+	+	+	+	+

| SNUM | SNAME	| MAJOR | DOB	| SEM |

\+	+	+	+	+	+

| 1001 | CHETHAN	| ISE  | 2000-11-03 |	4 |

| 1002 | CHETHAN CHAVAN | ISE  | 2000-11-03 |	4 |

\+	+	+	+	+	+

2 rows in set (0.00 sec)





**ii) updating seleted records.**

**Syntax**: Update <tablename> set <col>=<exp>, <col>=<exp> where <condition>; 

mysql> UPDATE STUDENT SET MAJOR='ECE' WHERE SNUM=1001;





