# Set Proxy Configuration File

The `networksetup` utility allows you to change the network settings from the command line.

To set an URL for an automatic proxy configuration (.pac) file, type the following command:

```
networksetup -setautoproxyurl <networkservice> <url>
```

Example:

```
networksetup -setautoproxyurl "Wi-Fi" "http://example.com/proxy.pac"
```

You can also create an alias in your `~/.bashrc` or `~/.zshrc` file:

```
alias setpac='networksetup -setautoproxyurl "USB Ethernet" "http://example.org/proxy.pac"'
```

More info: `man networksetup`
