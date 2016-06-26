# Columnate Lists

The `column` utility take lists from standard input and formats them into multiple columns. 

Its `-t` option can be used to prettify the output of a command by creating a whitespace delimited table.

Example with the output of a `join` command:

```bash
$ join ?.txt
1 blue fish
2 green turtle
3 orange car
5 red pickle
$ join ?.txt | column -t
1  blue    fish
2  green   turtle
3  orange  car
5  red     pickle
```

More info: `man column`
