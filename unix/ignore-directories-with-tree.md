# Ignore Directories With Tree

The `tree` command list contents of directories in a tree-like format.

Using the `-I` flag, it is possible to ignore directories matching a pattern. For example, to include hidden (`-a`) but exclude `.git` directories:

```bash
$ tree -a -I '.git'
```

Use the pipe (`|`) to specify more than one pattern :

```bash
$ tree -a -I 'vendor|.git'  
```

