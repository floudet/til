# Activate Hot-Added vCPU

A hot-added processor (e.g. on a VMWare virtual machine) must be activated before it can be used. 

To do so, issue the following command as root:

```bash
for i in /sys/devices/system/cpu/cpu*/online; do echo "1" > "$i"; done
```

[source](https://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=1015501)

