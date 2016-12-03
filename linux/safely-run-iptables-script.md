# Safely Run iptables Script

This can prevent you from being locked out after updating your iptables script:

```bash
./firewall.sh; echo "Success - Press CTRL+C"; sleep 10; service iptables stop; 
```

If the changes you made make you accidentally lose your ssh connection, the firewall will be automatically disabled after 10 seconds.

If you're able to see the "Success - Press CTRL+C" message, just hit <kbd>Ctrl</kbd>+<kbd>C</kbd> to send a INT signal to the current process.

