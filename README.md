# oracle_pdb_ass_II_20251SEN081_Kelly_Leondry


## Overview of Tasks
This assignment focuses on Oracle Pluggable Database (PDB) administration and Oracle Enterprise Manager (OEM). The tasks include creating a Pluggable Database, deleting a Pluggable Database, and accessing and demonstrating the Oracle Enterprise Manager dashboard.


## Oracle Environment Used
The assignment was completed using Oracle Database 21c Enterprise Edition on Windows with SQL Developer used for database administration and SQL execution. Oracle Enterprise Manager was used to access and demonstrate the database environment.

## EXPLANATION OF EACH TASK

## First task: PDB Creation
Objective,
The objective of this task was to create a new Pluggable Database (PDB) within the Oracle Container Database (CDB).

Procedure,
On step by step procedure you have to make sure you are connected as SYS USER within the main container database (CDB$ROOT).
By using command ' SHOW CON_NAME;' to Display and verify if you are connected to CDB$ROOT in order to be allowed to create a PDB.

then i used the next command to create the PDB and the user and set the password and check if is well created

CREATE PLUGGABLE DATABASE ke_pdb_20251SEN081
ADMIN USER kelly_plsqlauca_20251SEN081 IDENTIFIED BY xxxxx
FILE_NAME_CONVERT = (
    'C:\ORACLE\ORADATA\ORCL\PDBSEED',
    'C:\ORACLE\ORADATA\ORCL\ke_pdb_20251SEN081'
);

[PDB Creation Evidence](screenshots/pdb_creation/1.Connection%20and%20Pdb_Creation.png)

Next step is to OPEN it and PUT IN SAVE STATE so that will be immediately in open state available to interact after opening oracle
[PDB Opening Evidence](screenshots/pdb_creation/2.pdb%20opening%20and%20access.png)



## Second Task: PDB Deletion
Objective of the task was to delete a created PDB so that it no longer available in the my database

Procedures number 1 is to use the command to remove the PDB you want to delete from Open mode to
Mount or closed mode by using command:
'ALTER PLUGGABLE DATABASE ke_pdb_20251SEN081 CLOSE IMMEDIATE;'

Next after closing now its time to remove or Drop PDB using this command:
'DROP PLUGGABLE DATABASE ke_pdb_20251SEN081 INCLUDING DATAFILES;'

Then use the command SHOW PDBS; to verify if the PDB is deleted.

[Second Task Evidence](screenshots/pdb_deletion/2.deletion_and_verification.png)

## THIRD TASK: Oracle Enterprise Manager (OEM)
Objective for this task was to log into and Access the OEM with Dashboard reflecting my Oracle environment
and the completed PDB tasks and Even Username visible on dashboard

Using SYS credentials and my OEM Address: https://localhost:5500/em tasks successfully completed
as required.
[Evidence 1](screenshots/oem_dashboard/oem_Log%20_in.png)
[Evidence 2](screenshots/oem_dashboard/PDB_presence_in_oem.png)

## Challenges faced And Solutions

1. PDB Creation Syntax
During PDB creation, an ORA-02000: missing = keyword error was encountered. The issue was caused by incorrect SQL syntax. The command was reviewed and corrected according to the Oracle PDB creation syntax, after which the PDB was successfully created.
2. Understanding PDB and CDB
Initially, there was some difficulty distinguishing between the Container Database (CDB) and Pluggable Database (PDB).
This was resolved by making more research and understanding not memorising only the concept only then check the current container using SHOW CON_NAME and listing available PDBs using SHOW PDBS.

## Integrity statement

I declare that the work presented in this assignment is my own work. I have followed the academic integrity requirements of the course and have appropriately acknowledged any external resources used. The commands, configurations, screenshots, and explanations presented in this repository represent the work completed for this assignment.

## 


