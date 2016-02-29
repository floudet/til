# Format JSON

Formatting JSON can be achieved by using Vim's ability to run utilities without leaving the editor. 

```
:%!python -m json.tool
```

A key map can be created in your `.vimrc`. The example below will map the command to <kbd>=</kbd><kbd>j</kbd>

```
nmap =j :%!python -m json.tool<CR>
```

[Source](https://coderwall.com/p/faceag/format-json-in-vim)
