# Find Block Size

The following command can be used to find the block size of a ext2/ext3/ext4 partition:

```bash
# tune2fs -l /dev/sdb2 | grep -i 'block size'
Block size:               1024
```

Replace `/dev/sdb2` by the device name of the partition you want to check.

[Source](http://www.linfo.org/get_block_size.html)
