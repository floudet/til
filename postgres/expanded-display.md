# Expanded Display 

When using MySQL in command line, if you terminate a `select` query with `\G` it will display the results vertically.

You can achieve the same result in PostgreSQL by enabling *Expanded display* with the `\x` option.

It's a toggle, so you have to enable it before submitting the query.

```
database=> \x
Expanded display is on.
sdatabase=> select * from mytable;
```


