# Knife Show Nested Attributes

If you want to see the value of a nested attribute for a specific node, use knife search and a dot (`.`) to separate the levels of data:

```bash
knife search node name:<node_name> -a <main_attribute>.<nested_attribute>
```

Example:
```bash
knife search node name:myserver01 -a kernel.os
1 items found

myserver01:
  kernel.os: GNU/Linux
```

[Source](http://www.programmersparadox.com/2013/02/05/viewing-chef-node-attributes-with-knife/)
