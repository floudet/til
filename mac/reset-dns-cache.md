# Reset DNS Cache

OS X keeps a local cache of resolved DNS queries for a time defined by the DNS server. Sometimes it might be necessary to reset the cache immediately and re-query a DNS server.

Use the following Terminal command to reset the DNS cache in OS X v10.10.4 or later:
```
sudo killall -HUP mDNSResponder
```

[source](https://support.apple.com/en-us/HT202516)

