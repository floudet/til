# Create File With head

The -c option of the `head` command can be used to create files of a definite size.

For example, to create a 500MB file containing all zeroes to be used as swap: 

```bash
head -c 500MB /dev/zero > /swapfile
```

[Source](https://eklitzke.org/the-cult-of-dd)
