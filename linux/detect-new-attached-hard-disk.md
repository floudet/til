# Detect New Attached Hard Disk

A newly attached hard disk (e.g. on a VMWare virtual machine) won't be automatically seen by the OS. 

A two steps process is necessary to do so:

First, get the host bus number by issuing the following command as root:

```bash
grep mpt /sys/class/scsi_host/host?/proc_name

/sys/class/scsi_host/host2/proc_name:mptspi
```

In that example, the host is host2.

Then, use the command below to force disk detection:

```bash
echo "- - -" > /sys/class/scsi_host/host2/scan
```

Sample output:
```
root@tianhe-2:~# grep mpt /sys/class/scsi_host/host?/proc_name
/sys/class/scsi_host/host3/proc_name:mptspi
root@tianhe-2:~# echo "- - -" > /sys/class/scsi_host/host3/scan
root@tianhe-2:~# dmesg | tail
[45918306.640460] scsi target3:0:1: Ending Domain Validation
[45918306.640490] scsi target3:0:1: FAST-40 WIDE SCSI 80.0 MB/s ST (25 ns, offset 127)
[45918306.640826] sd 3:0:1:0: [sdd] 167772160 512-byte logical blocks: (85.8 GB/80.0 GiB)
[45918306.640870] sd 3:0:1:0: [sdd] Write Protect is off
[45918306.640873] sd 3:0:1:0: [sdd] Mode Sense: 61 00 00 00
[45918306.640918] sd 3:0:1:0: [sdd] Cache data unavailable
[45918306.640921] sd 3:0:1:0: [sdd] Assuming drive cache: write through
[45918306.641475] sd 3:0:1:0: Attached scsi generic sg4 type 0
[45918306.662092]  sdd: unknown partition table
[45918306.662304] sd 3:0:1:0: [sdd] Attached SCSI disk
```

[source](http://www.golinuxhub.com/2014/07/how-to-detect-new-hard-disk-attached.html)

