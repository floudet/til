# grep UTF-16

`grep` won't work on a UTF-16 encoded file:

```bash
$ file myfile.txt
myfile.txt: Little-endian UTF-16 Unicode text, with CRLF, CR line terminators
$ cat myfile.txt
��There is no knowledge
that is not power
$ grep is myfile.txt
$
```

To be able to use `grep` on such files you can convert them to UTF-8 with `iconv` and pipe the output to grep:

```bash
$ iconv -f utf-16 -t utf-8 myfile.txt | grep is
There is no knowledge
that is not power
```

You can also define this handy function in your `~/.bashrc` or `~/.zshrc` file:

```
greputf16 () {
    grep ${@:1:$(($#-1))} <(iconv -f utf-16 -t utf-8 ${@: -1}) | cut -d':' -f2
}
```

Use it the same way as you would with grep:

```bash
$ greputf16 is myfile.txt
There is no knowledge
that is not power
```

