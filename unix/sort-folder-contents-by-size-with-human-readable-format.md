# Sort Folder Contents By Size With Human Readable Format

The `du -hs *` command summarize disk usage for the current directory, and print sizes in human readable format (e.g., 1K 234M 2G).

Piping this command to sort however doesn't sort sizes properly. 

In the "recent" versions of GNU coreutils (>= 7.5), `sort` now includes a `-h` option to address this issue.

```
du -hs * | sort -h
```


##Workarounds if stuck with older versions:##

Use du `-B` option to scale sizes by M (or another unit) before printing them:
```
du -BM | sort -nr
```

Duplicate counting using xargs:
```
du | sort -nr | cut -f2- | xargs du -hs
```

Lengthy command for scripts or aliases:
```
du -sk * | sort -nr | while read size fname; do for unit in k M G T P E Z Y; do if [ $size -lt 1024 ]; then echo -e "${size}${unit}\t${fname}"; break; fi; size=$((size/1024)); done; done
```

