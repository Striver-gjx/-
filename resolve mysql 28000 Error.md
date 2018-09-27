## Ubantu MySQL ERROR 1698 (28000) 错误解决

```text
1.sudo service mysql stop
2.sudo mysqld_safe --skip-grant-tables &
3.SELECT user,host,plugin FROM mysql.user;
4.UPDATE mysql.user SET authentication_string=PASSWORD('123456'), plugin='mysql_native_password' WHERE user='root';
5.FLUSH PRIVILEGES;
6.sudo service mysql stop
7.sudo service mysql start
8.mysql -u root -p
9.enter your password just set in the update sql
10.login successful
```

