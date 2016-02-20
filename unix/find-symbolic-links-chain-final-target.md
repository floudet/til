# Find Symbolic Links Chain Final Target

To find the final target of a chain of symbolic links, use the `readlink` program with the `-e` option:

```bash
$ ls -l /usr/bin/awk
lrwxrwxrwx 1 root root 21 Jul  1  2015 /usr/bin/awk -> /etc/alternatives/awk
$ ls -l /etc/alternatives/awk
lrwxrwxrwx 1 root root 13 Jul  1  2015 /etc/alternatives/awk -> /usr/bin/gawk
$ readlink -e /usr/bin/awk
/usr/bin/gawk
```

