# Disable Binlogs When Restoring Dump

One might want to avoid writing binary logs when restoring a MySQL dump from the command line. Here is a way to achieve that:

```
$ (echo "set session sql_log_bin=0;" ; cat dump.sql) | mysql
```

[Source](https://geert.vanderkelen.org/2009/disabling-binary-logging-when-restoring-a-mysql-dump/)
