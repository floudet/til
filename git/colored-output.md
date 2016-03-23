# Colored Output

Git can color its output to your terminal, which is particularly appreciable when using commands like `git diff`.

Turn on all the default terminal coloring:
```
git config --global color.ui true
```

Or manually add the following in your `~/.gitconfig`:
```
[color]
        ui = true
```

[Source and more info](https://git-scm.com/book/no-nb/v1/Customizing-Git-Git-Configuration)
