# Simulate The Cron Environment 

Cron only provides a limited environment. To simulate it to test run your scripts first add this to your cron:

```bash
* * * * * env > ~/cronenv
```

After it runs, enter the environment by typing:

```bash
env - `cat ~/cronenv` /bin/sh
```

