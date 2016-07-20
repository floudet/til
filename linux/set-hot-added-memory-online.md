# Set Hot-Added Memory Online

Hot-added memory (e.g. on a VMWare virtual machine) must be set online before it can be used. 

To do so, issue the following command as root:

```bash
for ii in $(grep offline /sys/devices/system/memory/*/state | cut -d':' -f1); do echo online > $ii; done
```

[source](https://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=1012764)

