# grep Include Adjacent Lines

You may find yourself in a situation where you want to include next or previous lines to grep output in addition to the matching lines. 

This can be achieved by using the -A or -B options.

From the man page:
```
-A NUM, --after-context=NUM
              Print NUM lines of trailing context after matching lines.  Places a line containing a group  separator  (--)  between
              contiguous groups of matches.  With the -o or --only-matching option, this has no effect and a warning is given.

-B NUM, --before-context=NUM
              Print  NUM  lines  of leading context before matching lines.  Places a line containing a group separator (--) between
              contiguous groups of matches.  With the -o or --only-matching option, this has no effect and a warning is given.
```

For example, to include the next line:
```bash
grep -A1 'blah' file
```

Include 2 lines:
```bash
grep -A2 'blah' file
```

Another example, using the [books.xml Sample file from Microsoft](https://msdn.microsoft.com/en-us/library/ms762271(v=vs.85).aspx). Let's say you want the list of romance books along with their author:
```
$ grep -B2 'Romance' books.xml
      <author>Randall, Cynthia</author>
      <title>Lover Birds</title>
      <genre>Romance</genre>
--
      <author>Thurman, Paula</author>
      <title>Splish Splash</title>
      <genre>Romance</genre>
```

