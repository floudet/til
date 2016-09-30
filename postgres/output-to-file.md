# Output To File

It is possible to redirect query output to a file instead of displaying it on the screen.

Use `\o` to enable or disable this behavior:

```
database=> \o /path/to/file.txt
database=> select * from mytable;
database=> \o 
```

[Source](https://linuxconfig.org/saving-an-output-of-postgresql-query-to-a-text-file)
