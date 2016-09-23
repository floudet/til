# Multiple SSH Tunnels

Reaching more than one machine on a remote network using a jump host can be achieved with a single command. 

It's actually as easy as specifying the `-L` (or `-D`) option as much times as necessary (`-L` forward a local port to the given host and port on the remote side, `-D` does the opposite). 

On the example below, we want to open a RDP connection to 2 servers on a remote private network for which we can only reach a jump host through SSH from the outside.  

```bash
ssh -L 5905:172.16.0.20:3389 -L 5906:172.16.0.21:3389 floudet@bastion.example.com
```

Then on the local machine we just have to use our favorite RDC software and connect to localhost (127.0.0.1) port 5905 or 5906 to reach either server.  

[Source](https://www.phase2technology.com/blog/multiple-ssh-tunnels)
