# Format XML

As with JSON, formatting XML can be achieved by using Vim's ability to run utilities without leaving the editor. 

`xmllint` is probably the best command line tool to work with XML files.

```
:%!xmllint --format --recover - 2>/dev/null
```

On Debian-based systems, `xmllint` is part of the `libxml2-utils` package.

