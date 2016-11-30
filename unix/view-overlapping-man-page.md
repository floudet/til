# View Overlapping Man Page

Let's say you want to read the man page of the `openssl passwd` subcommand. Most likely `man passwd` will open the man page of the `passwd` command which is not the desired result. 

To deal with such overlapping first use `whatis` to display all available man pages with the same name as the one you're looking for.

```bash
~$ whatis passwd
passwd (5)           - the password file
passwd (1)           - change user password
passwd (1ssl)        - compute password hashes
```

Once we figured out which man page is the one we want to read, we use the identifier inside parenthesis to open it:

```bash
~$ man 1ssl passwd
```

[Source](https://www.cyberciti.biz/faq/linux-unix-view-man-pages-from-sections)
