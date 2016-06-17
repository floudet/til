# Get Hard Disk Detailed Info

`lshw` is a small tool to extract detailed information on the hardware configuration of the machine.

To get info about disks, use:

```
lshw -class disk
```

Sample output:
```
$ sudo lshw -class disk
  *-disk
       description: ATA Disk
       product: TOSHIBA MK1652GS
       vendor: Toshiba
       physical id: 0.0.0
       bus info: scsi@0:0.0.0
       logical name: /dev/sda
       version: 1D
       serial: 88LST8KOT
       size: 149GiB (160GB)
       capabilities: partitioned partitioned:dos
       configuration: ansiversion=5 logicalsectorsize=512 sectorsize=512 signature=a7ab1f0b
  *-cdrom
       description: DVD-RAM writer
       product: DVD+-RW TS-L633A
       vendor: TSSTcorp
       physical id: 0.0.0
       bus info: scsi@1:0.0.0
       logical name: /dev/cdrom
       logical name: /dev/cdrw
       logical name: /dev/dvd
       logical name: /dev/dvdrw
       logical name: /dev/sr0
       version: D500
       capabilities: removable audio cd-r cd-rw dvd dvd-r dvd-ram
       configuration: ansiversion=5 status=nodisc
```

