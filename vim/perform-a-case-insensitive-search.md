# Perform A Case Insensitive Search

When searching with `/` use the `\c` escape sequence to make your search case insensitive.

```
/\cblah
```

If you want all your searches to be case insensitive:

```
:set ic
```

You can also put `set ic` in your `.vimrc`

