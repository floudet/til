# Knife Search Nested Attributes

When using knife search to search nodes whose nested attributes have a specific value, use underscores (`_`) to separate the levels of data. 

For instance, if `knife node show -l mynode` returns something like this:
```bash
[...]
Platform:    debian 7.9
Tags:
Attributes:
Custom:
  Datacenter:      Seoul
  Department:      DevOps
  Vulnerabilities:
    check-dirtycow:   secure
    check-ghost:      secure
    check-shellshock: secure
build-essential:
  compile_time: true
[...]
```

Let's say you want to find all nodes with the attribute `[Custom][Datacenter] = Seoul`, your knife search will look like that:

```bash
knife search node 'Custom_Datacenter:Seoul' -i
```

[Source](https://docs.chef.io/knife_search.html#nested-fields)
