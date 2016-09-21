# ssh-copy-id On A Different Port

The man page of `ssh-copy-id` doesn't explain how to specify a different port than 22 to copy the public key to a remote machine.

It can actually be achieved by using a command similar to the one below. On this example, the port 22025 is used: 

```
$ ssh-copy-id "user@host -p 22025"
```

[Source](http://it-ride.blogspot.in/2009/11/use-ssh-copy-id-on-different-port.html)
