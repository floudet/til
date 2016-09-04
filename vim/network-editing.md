# Network Editing

"Recent" versions of Vim come with bundled [netrw](http://www.vim.org/scripts/script.php?script_id=1075) plugin. It allows to read and edit files accross networks.

For example, to edit a file on a remote machine over a SCP link:

```bash
vim scp://remoteuser@server.tld//absolute/path/to/document
```

or directly from Vim's command mode:
```
:e scp://remoteuser@server.tld//absolute/path/to/document
```

Using a relative path works too if the file to edit is contained within the home directory of the remote user:
```
:e scp://remoteuser@server.tld/relative/path/to/document
```


[Source](http://vim.wikia.com/wiki/Editing_remote_files_via_scp_in_vim)
