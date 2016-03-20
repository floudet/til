# Automatic Indentation

Vim have powerful built-in indentation capabilities. 

To enable them, the `autoindent` option should be turned on, and the indent files loaded:

```
set autoindent
filetype indent on
```

Then the `=` command will format lines based on a motion. So for indenting the whole file, one would type:

```
gg
=G
```

By default, vim already includes indent files for a large variety of programming languages. You can edit them, add new ones downloaded from the Internet or create your own. 

On Debian 7, these files are located in `/usr/share/vim/vim73/indent/`.

[Source and more info](http://vim.wikia.com/wiki/Indenting_source_code)

