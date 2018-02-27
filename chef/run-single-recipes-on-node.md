# Run Single Recipes On Node

Chef Client 12.0 introduces a new -o option allowing to replace the current run-list with the specified items.

It is useful to run single recipes on a node where chef-client is disabled, or on which chef-client fails because of an issue in another recipe. 

```bash
chef-client -o 'my_super_recipe'
```

[Source](https://docs.chef.io/ctl_chef_client.html)
