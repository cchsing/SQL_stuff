# MySQL

1. sudo apt install mysql-server
2. sudo systemctl start mysql.service
3. ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
4. CREATE USER 'username'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
5. GRANT PRIVILEGE ON database.table TO 'username'@'host';
6. GRANT CREATE, ALTER, DROP, INSERT, UPDATE, DELETE, SELECT, REFERENCES, RELOAD on _._ TO 'sammy'@'localhost' WITH GRANT OPTION;
7. GRANT ALL PRIVILEGES ON _._ TO 'sammy'@'localhost' WITH GRANT OPTION;
8. FLUSH PRIVILEGES;
9. systemctl status mysql.service
10. sudo mysqladmin -p -u sammy version

## Remote connection to the MySQL linux

### How to Allow Remote Connections to MySQL [URL](https://phoenixnap.com/kb/mysql-remote-connection)

- Change Bind-Address IP in configuration file

`sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf`

- Enable port connection through firewall
- Grant remote access privilege on database

  - `GRANT ALL PRIVILEGES ON yourDB.* TO user1@'133.155.44.103' IDENTIFIED BY 'password1';`

    - the password is changed at the same time and user is created if user does not exists

  - `CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';`

  - `GRANT ALL PRIVILEGES ON database.* TO 'username'@'localhost';`

- Grant existing user by updating records
  - `update db set Host='133.155.44.103' where Db='yourDB';`
  - `update user set Host='133.155.44.103' where user='user1';`
