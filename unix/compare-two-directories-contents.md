# Compare Two Directories Contents

This can be achieved using `diff` with its `-r` (recursive) and `-q` (quiet: output only differences) options:

```bash
diff -rq /path/to/foo /path/to/bar
```

Sample output:
```bash
$ diff -rq /path/to/foo /path/to/bar
Only in /path/to/foo: file2.txt
Files /path/to/foo/file3.txt and /path/to/bar/file3.txt differ
```

