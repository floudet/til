# Reset Auto Increment Counter

Postgres uses something called a sequence to keep track of the auto increment counts (when you use autoincrementing pseudotypes like serial or bigserial).

To list the sequences use:

```
\ds
```

The sequence name is in the format of ${table}_{variable}_seq

If you delete all the rows in a table using a sequence, the sequence will keep its last value and when you start inserting rows again, the sequence will be incremented starting from this value.

To reset the counter use:

```
alter sequence table_id_seq restart with 1;
```

Replace *table_id_seq* by the name of the sequence you want to reset.

[Source](http://digitaldreamer.net/blog/2013/6/11/reset-auto-increment-counter-postgres)

