# Show users credential in SQL

## Show all the users in databases

mysql -u root -p
SELECT user FROM mysql.user;

- show all users by running the query as root.

SELECT user,host FROM mysql.user;

## Display Unique Usernames

SELECT DISTINCT user FROM mysql.user;

test link [go to select](./SelectFromTables.md)

# Create User and Grant Permission to Database

1. mysql -u root -p
2. CREATE USER 'username'@'host'

   - 'host' hostname from which this user will connect.

3. CREATE USER 'sammy'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
4. GRANT CREATE, ALTER, DROP, INSERT, UPDATE, DELETE, SELECT, REFERENCES, RELOAD on _._ TO 'sammy'@'localhost' WITH GRANT OPTION;
5. GRANT ALL PRIVILEGES ON _._ TO 'sammy'@'localhost' WITH GRANT OPTION;
6. FLUSH PRIVILEGES;
7. REVOKE type_of_permission ON database_name.table_name FROM 'username'@'host';
8. SHOW GRANTS FOR 'username'@'host';
9. DROP USER 'username'@'localhost';
