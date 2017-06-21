# Replace Tabs with Spaces

Vim provides the `:retab` command that allows to replace all tabs to a number of spaces defined by `tabstop`. 

Set the number of spaces corresponding to 1 TAB
```
:set tabstop=4
```

expandtop has to be enabled
```
:set expandtab
```

Then to convert all tabs to spaces on the current buffer
```
:retab
```

To get more info about the `:retab` command
```
:help :retab
```
