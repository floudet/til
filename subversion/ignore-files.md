# Ignore Files

To ignore files in the current directory, use:

```bash
svn propedit svn:ignore .
```

This opens your default editor. Fill a list of files or directories to ignore, save and exit.

Ex:
```
/log
*.swp
todo.txt
```

To display the list:

```bash
svn propget svn:ignore
```

To find the files that are ignored:
```bash
svn status -u -v --no-ignore | grep "^I" | awk '{print $2}'
```

