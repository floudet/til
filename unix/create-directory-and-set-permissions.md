# Create Directory Set Permissions And Ownership 

Why run 3 commands when you can have the same result with only one? The `install` command allows you to create a directory, and set its permissions and ownership.

```bash
$ install -d -m 750 -o user newdir
```

Gives the same result as:

```bash
$ mkdir newdir && chown user newdir && chmod 750 newdir
```

