# Quickly Send Directory Over Network

A quick and dirty way to send a directory over the local network is to use netcat with tar.

On the target machine:
```bash
nc -l -p 9988 | tar xvzf -
```

On the source:
```bash
tar cvzf - dirtotransfer | nc 172.16.0.20 9988
```

Add encryption (Blowfish Cipher):

Target:
```bash
nc -l -p 9988 | openssl bf -d | tar xvzf -
```

Source:
```bash
tar cvzf - dirtotransfer | openssl bf -salt | nc 172.16.0.20 9988
```



