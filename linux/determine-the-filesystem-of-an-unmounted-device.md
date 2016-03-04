# Determine The Filesystem Of An Unmounted Device 

You can use `df` with the `-T` option to show the filesystem of a mounted partition:

```bash
# df -T /dev/sdc1
Filesystem     Type 1K-blocks  Used Available Use% Mounted on
/dev/sdc1      ext4   4127424 73720   3844040   2% /mnt/temp
```

But what if the partition is not mounted and you still want to know which filesystem it is holding on? 

The `blkid` program can help you find this information:

```bash
# blkid /dev/sdc1
/dev/sdc1: UUID="1d22aff1-7e59-43eb-b365-75669feea415" TYPE="ext4"
```

If you just need to extract the filesystem type (for scripting purposes for example):

```bash
# blkid -s TYPE -o value /dev/sdc1
ext4
```

