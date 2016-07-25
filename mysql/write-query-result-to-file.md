# Write Query Result To File

The `SELECT ... INTO OUTFILE` form of SELECT allows you to write the result of a query to a file:

For example, to store the list of users: 

```
mysql> select user,host from mysql.user into outfile '/tmp/mysql_users.txt';
```

[Source and more info](http://dev.mysql.com/doc/refman/5.7/en/select-into.html)
