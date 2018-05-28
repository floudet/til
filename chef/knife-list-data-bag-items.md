# Knife List Data Bag Items

Listing the data bags currently available on the Chef server is as easy as : 

```bash
knife data bag list <data_bag>
```

But to list the data bag items, you'll have to use knife search:

```bash
knife search <data_bag> "*:*"
```

To list only the IDs:

```bash
knife search <data_bag> "*:*" -i 
```

Combined with grep, this can be useful if you have a data bag deleted from source control but not from the Chef server and for which you forgot its exact name.
