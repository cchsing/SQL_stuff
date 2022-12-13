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
