# Pipe Output To root-owned File 

Ever find yourself in a situation where you try to redirect the output of a command to a file or directory on which only root have write access?

```bash
fabien@tianhe-2:~$ echo "hello world" > /root/file.txt
-bash: /root/file.txt: Permission denied
fabien@tianhe-2:~$ sudo !!
sudo echo "hello world" > /root/file.txt
-bash: /root/file.txt: Permission denied
```

In the example above the `sudo` command doesn't work because the redirection is executed by the shell and the shell doesn't run as root. This limitation can be overcomed by using `tee`:

```bash
fabien@tianhe-2:~$ echo "hello world" | sudo tee /root/file.txt > /dev/null
fabien@tianhe-2:~$ sudo cat /root/file.txt
hello world
```

Another solution, more expensive resources-wise, is to call a new shell with the `-c` option (supported by sh/bash/zsh):

```bash
fabien@tianhe-2:~$ sudo sh -c "echo hello world > /root/file.txt"
fabien@tianhe-2:~$ sudo cat /root/file.txt
hello world
```
