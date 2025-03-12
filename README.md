# DATABASE-BACKUP-AND-RECOVERY
COMPANY: CODTECH IT SOLUTIONS

NAME: SUSHIL SUBHASH PANDE

INTERN ID: CT08VIC

DOMAIN: SQL

DURATION:4 WEEKS

MENTOR: NEELA SANTOSH

DESCRIPTION 

This task involves creating and managing a student table in MySQL, PostgreSQL, and SQL Server, focusing on inserting data, simulating restoration, and performing backup and restore operations.

1. Creating the Student Table:
The student table is created with columns:
•	student_id: Auto-incremented primary key.
•	first_name: Student's first name (non-null).
•	last_name: Student's last name (non-null).
•	date_of_birth: Student's birth date.
•	email: Unique email address of the student.
SQL Command:
CREATE TABLE student (
    student_id INT AUTO_INCREMENT PRIMARY KEY,
    first_name VARCHAR(100) NOT NULL,
    last_name VARCHAR(100) NOT NULL,
    date_of_birth DATE,
    email VARCHAR(100) UNIQUE
);

2. Inserting Data into the Student Table:
Sample student data is inserted into the table.
SQL Command:
INSERT INTO student (first_name, last_name, date_of_birth, email)
VALUES ('Bhavesh', 'Borekar', '2006-10-27', 'bhavesh@gmail.com'),
       ('Sushil', 'Pandey', '2005-08-22', 'sushil@gmail.com'),
       ('Payal', 'Khade', '2005-02-10', 'payal@gmail.com');

3. Simulating Data Restoration:
Data restoration is simulated by re-inserting the same records, mimicking a restore from a backup.
SQL Command:
INSERT INTO student (first_name, last_name, date_of_birth, email)
VALUES ('Bhavesh', 'Borekar', '2006-10-27', 'bhavesh@gmail.com'),
       ('Sushil', 'Pandey', '2005-08-22', 'sushil@gmail.com'),
       ('Payal', 'Khade', '2005-02-10', 'payal@gmail.com');

4. Backup and Restore in MySQL:
Backup Process:
•	The mysqldump command is used to back up the database into an SQL file (task4.sql). 
o	Command:
•	mysqldump -u root -p student > task4.sql
Restore Process:
•	The mysql command is used to restore data from the backup file. 
o	Command:
•	mysql -u root -p student < task4.sql

5. Backup and Restore in PostgreSQL:
Backup Process:
•	PostgreSQL's pg_dump command backs up the data into a custom .dump format. 
o	Command:
•	pg_dump -U postgres -W -F c student > task4.dump
Restore Process:
•	The pg_restore command is used to restore the data from the .dump file. 
o	Command:
•	pg_restore -U postgres -d student -W task4.dump

6. Backup and Restore in SQL Server:
Backup Process (T-SQL):
•	The BACKUP DATABASE command is used to back up the database to a .bak file. 
o	Command:
•	BACKUP DATABASE database2 TO DISK = 'C:\user\task4.bak';
Restore Process (T-SQL):
•	The RESTORE DATABASE command is used to restore the database from the .bak file. 
o	Command:
•	RESTORE DATABASE database2 FROM DISK = 'C:\user\task4.bak';

This task demonstrates:
•	How to create and manage a student table in MySQL, PostgreSQL, and SQL Server.
•	The process of inserting, simulating, and verifying data restoration.
•	Backup and restore techniques using commands like mysqldump, pg_dump, and SQL Server's BACKUP and RESTORE.

OUTPUT

![TASK4 1](https://github.com/user-attachments/assets/9d8c6ea0-58e9-4561-b2ca-b207db4d135f)


![TASK4 2](https://github.com/user-attachments/assets/7fdf62bc-0d30-4fcc-9660-3ed8d44be531)
