# Show Databases in SQL

## Login

mysql -u <user> -p

## list all the databases that the <user> has permission to

SHOW DATABASES;

USE {DATABASE};

SHOW SCHEMAS;

## show databases with specific pattern or naming rules

SHOW DATABASES LIKE \<pattern\>; <br>
SHOW DATABASES LIKE 'open%';

- The percent sign (%) means zero, one, or multiple characters.

## show databases from CLI

mysql -u <user> -p -e 'show databases;' <br>
mysqlshow -u <user> -p

# Creating Database

1. CREATE DATABASE django_db_1;
