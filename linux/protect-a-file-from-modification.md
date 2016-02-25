# Protect A File From Modification

`chattr` (Change Attribute) is a command line Linux utility that is used to set/unset certain attributes to a file in Linux system to secure accidental deletion or modification of important files and folders, even though you are logged in as *root*.

For example, it can be used to write protect /etc/resolv.conf from being updated by dhclient:

```bash
# chattr +i /etc/resolv.conf
```

A file with the i (immutable) attribute cannot be modified. It cannot be deleted or renamed, no link can be created to this file and no data can be written to the file. When set, prevents, even *root*, from erasing or changing the contents of the file.

To reset back permission, type the following command:

```bash
# chattr -i /etc/resolv.conf
```

Use the `lsattr` command to see attributes set by `chattr`.

```bash
# lsattr /etc/resolv.conf
----i--------e- /etc/resolv.conf
```

[source](http://www.cyberciti.biz/faq/how-to-make-a-file-unchangeable-unalterable-so-that-no-one-can-modify-it/)

