# ls File Size Unit 

By default, `ls -l` displays the files size in bytes.

```
$ ls -lh
total 11M
-rw-r--r-- 1 floudet floudet 10M Sep  7 17:04 file1.txt
-rw-r--r-- 1 floudet floudet 15K Sep  7 17:05 file2.txt
-rw-r--r-- 1 floudet floudet   5 Sep  7 17:05 file3.txt
```

You can use `ls -lh` to display the file sizes in human readable format:

```
$ ls -lh
total 11M
-rw-r--r-- 1 floudet floudet 10M Sep  7 17:04 file1.txt
-rw-r--r-- 1 floudet floudet 15K Sep  7 17:05 file2.txt
-rw-r--r-- 1 floudet floudet   5 Sep  7 17:05 file3.txt
```

But what if you want the file sizes displayed using a specific unit? This can be achieved using the `--block-size` option:

```
$ ls -l --block-size=K
total 10260K
-rw-r--r-- 1 floudet floudet 10240K Sep  7 17:04 file1.txt
-rw-r--r-- 1 floudet floudet    15K Sep  7 17:05 file2.txt
-rw-r--r-- 1 floudet floudet     1K Sep  7 17:05 file3.txt
```

When using this option, file sizes are rounded up to the nearest unit you specified. On the example below, even though we have a 5 bytes file and a 15 kilobytes file, they're both displayed as having a size of 1M:

```
$ ls -l --block-size=M
total 11M
-rw-r--r-- 1 floudet floudet 10M Sep  7 17:04 file1.txt
-rw-r--r-- 1 floudet floudet  1M Sep  7 17:05 file2.txt
-rw-r--r-- 1 floudet floudet  1M Sep  7 17:05 file3.txt
```

