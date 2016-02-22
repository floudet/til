# Disable Sleep After Locking Screen

By default my Mac (OSX 10.10) was going to sleep after locking the screen, resulting in a loss of connectivity (Dropping SSH connections etc).

The solution:
```
sudo pmset -a sleep 0
```

Revert:
```
sudo pmset -a sleep 1
```

[source](http://apple.stackexchange.com/questions/120639/how-can-i-stop-my-macbook-pro-from-automatically-sleeping-when-i-lock-the-screen)
