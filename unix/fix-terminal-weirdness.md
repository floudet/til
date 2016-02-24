# Fix Terminal Weirdness

If your shell gets confused (as can often happen if you output binary data to it) and starts displaying gibberish, try entering:

```bash
$ stty sane
```

That will usually succeed in bringing the shell to reason and making it operate as expected again.

The `reset` command is also often effective at fixing a messed up terminal.

source: *Running Linux, 5th Edition - O'Reilly* 

