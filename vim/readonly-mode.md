# Readonly Mode

Vim can be started in read-only mode by using `view`:

```
view <file>
```

It can also be done with the `-R` argument.

Be careful of performance issues when used to open large files (typically logs). Use of `less` may be prefered in that case.

