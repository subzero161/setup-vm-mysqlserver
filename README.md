# How to setup a mysql in a VM, Instructions taken from HHA 504, AHI, SBU

## Setting up MySQL

###### Step 1: Update OS
    sudo apt-get update

###### Step 2: Install MySQL
    sudo apt install mysql-server mysql-client

###### Step 3: Log into MySQL
    sudo mysql
    
###### Step 4: Check all available databases installed
    show databases;

###### Step 4: Copy and Paste the next line of code
    eval $(/opt/homebrew/bin/brew shellenv)

## Creating a new user in the database
###### Step 1: Change username and password to what you want
    CREATE USER 'username'@'%' IDENTIFIED BY 'password';

###### Step 2: Check to cofirm user exists
    select user from mysql.user;

###### Step 3: Gran privileges to the user you created
    GRANT ALL PRIVILEGES ON *.* TO 'username'@'%' WITH GRANT OPTION;

###### Step 4: Check to confirm user granted privelege
    show grants for username;
    
###### Step 5: Quit out of MySQL
    \q
    
###### Step 6: Test local user connection from linux terminal
    mysql -u username -p
###### You will be prompted for password from step 1, type that into terminal

## Creating a Data base
###### Step 1: Create database
    create database databasename;

###### Step 2: Check to see if databases were created
    show databases;


