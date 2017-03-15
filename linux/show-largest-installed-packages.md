# Show Largest Installed Packages

`debian-goodies` is a package available for Debian/Ubuntu distros and containing a set of command line utilities.

Among them `dpigs` allows to find the packages installed on the system that occupy the most space. Use the `-H` option to display the sizes in human-readable format.

```bash
fabien@tianhe-2:~$ sudo dpigs -H
 101.1M linux-image-3.2.0-4-amd64
  30.3M python2.7-dev
  22.1M libicu48
  21.8M vim-runtime
  17.4M gcc-4.7
  16.8M linux-headers-3.2.0-4-common
  16.7M perl
  15.7M g++-4.7
  15.0M gcc-4.6
  14.8M locales
```
