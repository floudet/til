# Reduce Consecutive Spaces

Reducing all consecutive spaces on the current buffer can be achieved in (at least) 2 different ways:

Calling the shell and the `tr` utility:

```
:%!tr -s ' '
```

Using regular expressions:

```
s/ \{2,}/ /g
```

