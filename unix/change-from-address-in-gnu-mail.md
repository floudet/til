# Change From Address In GNU Mail

By default, the `mail` command from `mailutils` sends email as `$USER@$HOSTNAME`.

GNU mail have a `-a` option that allow to specify additional headers.

```bash
echo "This is a test" | mail -aFrom:testing@example.com -s "Testing" recipient@example.org
```

