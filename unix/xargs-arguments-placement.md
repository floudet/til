# xargs Arguments Placement

`xargs` is a tool that allows to build and execute command lines from standard input. 

If you want the listed arguments to be inserted in the middle of the command line, you can use the `-I` flag. It takes a string that will be replaced with the supplied input before the command is executed.

Example to move all files with the .bak extension to the ~/old directory:

```bash
$ find . -name "*.bak" -print0 | xargs -0 -I {} mv {} ~/old
```

[Source](http://offbytwo.com/2011/06/26/things-you-didnt-know-about-xargs.html)
