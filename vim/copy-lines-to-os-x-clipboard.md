# Copy Lines To OS X Clipboard

You can visually select a line and use the following command:

```
:w !pbcopy
```

This only work with whole lines. If you select part of a line the whole line will still be copied to the clipboard.

For convenience, a key map can be created in your `.vimrc` file: 

```
vmap <C-c> :w !pbcopy<CR><CR>
```

With this setup, <kbd>Control</kbd>+<kbd>C</kbd> will copy the text to the clipboard when you are in visual mode.

