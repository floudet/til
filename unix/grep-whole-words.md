# grep Whole Words

The easiest way to use `grep` to select only lines containing matches that form whole words is to use its `-w` option:

Without:
```bash
$ grep learn /usr/share/dict/words
clearness
clearness's
learn
learned
learner
learner's
learners
learning
...
```

With:
```bash
$ grep -w learn /usr/share/dict/words
learn
```

However, the hyphen (-) is not considered by grep as a word constituent character. If you want to exclude lines with "hyphenated" versions of the word you're searching, you'll have to use the extended regexps (`-E` option):

```bash
$ cat file.txt
goodies
good-looking
good
good-hearted

$ grep -w good file.txt
good-looking
good
good-hearted

$ grep -E '\<good\>([^-]|$)' file.txt
good
```

