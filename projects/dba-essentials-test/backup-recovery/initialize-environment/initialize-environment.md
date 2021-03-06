# Initialize environment

## Introduction
In this lab, we will review and startup all components required to run this workshop successfully.

Estimated Time: 5 minutes

### Objectives
- Set up the components required for performing this workshop.

### Prerequisites
- A Free Tier, Paid or LiveLabs Oracle Cloud account.
- You have completed:
    - Lab: Prepare setup (_Free-Tier_ and _Paid Tenants_ only)


## Task 1: Set the environment
To connect to Oracle Database and run SQL commands, you should set the environment first. 

In this task, you set up the environment using the following steps.

1. Log in to your host as `oracle`, the user who can perform database administration.

2. Open a terminal window and change the current working directory to `$ORACLE_HOME/bin`.
    ```
    $ <copy>cd /opt/oracle/product/21c/dbhome_1/bin</copy>
    ```

3. Run the command `oraenv` to set the environment variables.
    ```
    $ <copy>./oraenv</copy>
    ```

4. Enter Oracle SID `CDB1`.
    ```
    ORACLE_SID = [oracle] ? <copy>CDB1</copy>

    The Oracle base has been set to /opt/oracle
    ```
    This command also sets the Oracle home path to `/opt/oracle/product/21c/dbhome_1`.

You have set the environment variables for the active terminal session. You can now connect to Oracle Database and run the commands.

>**Note:** Every time you open a new terminal window, you need to set the environment variables to connect to Oracle Database from that terminal. Environment variables from one terminal do not apply automatically to other terminals. 

Alternatively, you may run the script file `.set-env-db.sh` from the home location and enter the number for `ORACLE_SID`, for example, `3` for `CDB1`. It sets the environment variables automatically.

## Task 2: Download and execute the SQL script file

In this task, you download and execute the SQL script file using the following steps.

1. Download and save the [backup-and-recovery-operations-prerequisities.sql](backup-and-recovery-operations-prerequisities.sql) script file.

2. Open the backup-and-recovery-operations-prerequisities.sql and update the following details in the script file.
    * password - Provide your password.
    * host name - Provide the host name of the machine where the database is installed.
    * port - Provide the port name. Usually port number is 1521.

3. Start the SQL\*Plus prompt and connect as the sysdba user.
    ```
    $ <copy>./sqlplus / as sysdba</copy>
    ```
    Output:
    ```
    SQL*Plus: Release 21.0.0.0.0 - Production on Thu Dec 16 07:31:06 2021
    Version 21.3.0.0.0

    Copyright (c) 1982, 2021, Oracle.  All rights reserved.

    Connected to:
    Oracle Database 21c Enterprise Edition Release 21.0.0.0.0 - Production
    Version 21.3.0.0.0
    ```

4. Run the following command to run the SQL script file.
    ```
    SQL> <copy>START backup-and-recovery-operations-prerequisities.sql</copy>
    ```

5. Exit the SQL\*Plus prompt.


You may now **proceed to the next lab**.


## Acknowledgements
- **Author**: Suresh Mohan, Database User Assistance Development Team
- **Contributors**: Suresh Rajan, Manish Garodia
- **Last Updated By & Date**: Suresh Mohan, May 2022
