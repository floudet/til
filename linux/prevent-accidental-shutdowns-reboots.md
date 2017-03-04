# Prevent Accidental Shutdowns and Reboots

Debian based distributions offers a package named `molly-guard`. It is a utility preventing yourself to accidentally reboot or shutdown the wrong system. 

Once installed, it will override the existing `shutdown/reboot/halt/poweroff` commands by asking you to type the hostname of the machine, in order to confirm that it is really what you intended to do.

Example:

```bash
fabien@tianhe-2:~$ sudo reboot
W: molly-guard: SSH session detected!
Please type in hostname of the machine to reboot: ^C
Good thing I asked; I won't reboot tianhe-2 ...
W: aborting reboot due to 30-query-hostname exiting with code 1.
```

[Source](http://www.2daygeek.com/molly-guard-protects-machines-from-accidental-shutdowns-reboots/)
