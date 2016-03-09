# Use A pgpass File To Avoid Typing Passwords

It is convenient to have a `~/.pgpass` file to avoid regularly having to type in passwords.

The password in the file will be used if the connection requires a password and no password has been specified otherwise. 

This file should contain lines of the following format:

```
hostname:port:database:username:password
```

On Unix systems, the permissions on `.pgpass` must disallow any access to world or group. Achieve this by the command `chmod 0600 ~/.pgpass`. If the permissions are less strict than this, the file will be ignored.

[Source](http://www.postgresql.org/docs/9.5/static/libpq-pgpass.html)

