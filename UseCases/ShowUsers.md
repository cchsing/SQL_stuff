# Show users credential in SQL

## Show all the users in databases

mysql -u root -p
SELECT user FROM mysql.user;

- show all users by running the query as root.

SELECT user,host FROM mysql.user;

## Display Unique Usernames

SELECT DISTINCT user FROM mysql.user;
