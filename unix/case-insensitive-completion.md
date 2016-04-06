# Case Insensitive Completion

Bash's default tab-completion for filenames is case-sensitive. To make it case insensitive, type:

```bash
$ bind 'set completion-ignore-case on'
```

Put the following line in a `~/.inputrc` (single user) or `/etc/inputrc` (all users) file to make it permanent:

```
set completion-ignore-case on
```

Note: This **doesn't work** with Zsh.


[Source](http://www.cyberciti.biz/faq/bash-shell-setup-filename-tab-completion-case-insensitive)
