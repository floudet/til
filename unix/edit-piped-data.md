# Edit Piped Data

The `vipe` program from the `moreutils` package allows to "insert a text editor into a pipe". That is, run your `EDITOR` in the middle of a unix pipeline and edit the data that is piped. 

```bash
command1 | vipe | command2
```

This is useful when installing softwares using the `curl ... | sh` method, to make sure the installation script won't do anything harmful to your system. 

If you're using Vim, and want to abort piping to the second command, exit with `:cq` (quit Vim with a non-zero exit code). 

