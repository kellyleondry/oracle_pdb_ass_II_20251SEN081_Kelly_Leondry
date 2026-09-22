# oracle_pdb_ass_II_20251SEN081_Kelly_Leondry


## 1. Overview of Tasks
This assignment focuses on Oracle Pluggable Database (PDB) administration and Oracle Enterprise Manager (OEM). The tasks include creating a Pluggable Database, deleting a Pluggable Database, and accessing and demonstrating the Oracle Enterprise Manager dashboard.


## 2. Oracle Environment Used
The assignment was completed using Oracle Database 21c Enterprise Edition on Windows with SQL Developer used for database administration and SQL execution. Oracle Enterprise Manager was used to access and demonstrate the database environment.

## 3. EXPLANATION OF EACH TASK

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

Then use the command SHOW PDBS; to verify if the PDB is deleted

[Second Task Evidence](screenshots/pdb_deletion/2.pdb%20deletion%20and%20verification.png)

## THIRD TASK: Oracle Enterprise Manager (OEM)
Objective for this task was to log into and Access the OEM with Dashboard reflecting my Oracle environment
and the completed PDB tasks and Even Username visible on dashboard

Using SYS credentials and my OEM Address: https://localhost:5500/em tasks successfully completed
as required.
[Evidence 1](screenshots/oem_dashboard/oem_Log%20_in.png)
[Evidence 2]()


