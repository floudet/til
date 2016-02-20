# Find Symbolic Links Chain Final Target

To find the final target of a chain of symbolic links, use the `readlink` program with the `-e` option.

For example, on one system we have `/usr/bin/awk` which is a symbolic link to `/etc/alternatives/awk`. The latter being itself a symbolic link pointing to `/usr/bin/gawk` as we can figure out with the `ls -l` command:

```bash
$ ls -l /usr/bin/awk
lrwxrwxrwx 1 root root 21 Jul  1  2015 /usr/bin/awk -> /etc/alternatives/awk

$ ls -l /etc/alternatives/awk
lrwxrwxrwx 1 root root 13 Jul  1  2015 /etc/alternatives/awk -> /usr/bin/gawk
```

`readlink -e` gives us the final target:

```bash
$ readlink -e /usr/bin/awk
/usr/bin/gawk
```

