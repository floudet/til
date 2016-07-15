# Replace Newlines

You can use the `tr` utility to replace newline by another character:

In the example below, we replace the newline characters by spaces in stdin. This command lists all users on the system side by side:

```bash
cat /etc/passwd | cut -d':' -f1 | tr '\n' ' '
```

