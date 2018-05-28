# Knife List Data Bag Items

Listing the data bags currently available on the Chef server is as easy as : 

```bash
knife data bag list
```

But to list the data bag items, you'll have to use knife search:

```bash
knife search Nagios_Services "*:*"
```

To list only the IDs:

```bash
knife search Nagios_Services "*:*" -i 
```

Combined with grep, this can be useful if you have a data bag deleted from source control but not from the Chef server and for which you forgot its exact name.
