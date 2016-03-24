# Is My Terminal A Screen

To know whether you're in a screen session or not, check the $STY or $TERM environment variables.

Not in screen:
```bash
$ echo $STY

$ echo $TERM
xterm-256color
```

In screen:
```bash
$ echo $STY
22543.pts-0.floudet-test
$ echo $TERM
screen
```

Code samples to check if a bash script is run inside a screen:
```bash
if [ -z "$STY" ]; then
    echo "This script must be run inside a screen."
    exit 1;
fi
```

```bash
if [ "$TERM" != "screen" ]; then
    echo "This script must be run inside a screen."
    exit 1;
fi
```

