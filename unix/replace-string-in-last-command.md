# Replace String In Last Command

Bash provide features called *event designators*. 

One of these allows you to repeat the last command, substituting one string with another:  

**^***string1***^***string2*

Example for path replacement:

```bash
~$ cd /usr/share/mqn/man1/
-bash: cd: /usr/share/mqn/man1/: No such file or directory
~$ ^mqn^man
cd /usr/share/man/man1/
/usr/share/man/man1$
```

Source: *Learning the bash Shell, 3rd Edition - O'Reilly* (p.165) 

