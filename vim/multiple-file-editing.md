# Multiple File Editing

You can open multiple files at once by specifying their names one after the other as arguments when opening vim.

```
vim file1.txt file2.txt file3.txt
```

Once in vim use `:prev` and `:next` to switch between the files. 

You can also use the `-o` option to open each file into a window of its own.

```
vim -o file1.txt file2.txt file3.txt
```

`-O` does the same thing but with vertical splits.

```
vim -O file1.txt file2.txt file3.txt
```

