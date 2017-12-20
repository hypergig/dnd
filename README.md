# dnd
My Dungeons &amp; Dragons repo

# pdf diff magic
To get pdf diffing to work:

* install diff-pdf
```
brew install diff-pdf
```

* create a new difftool in your `~/.gitconfig` file
```
[difftool "pdf"]
cmd = diff-pdf --output-diff=/tmp/diff.pdf \"$REMOTE\" \"$LOCAL\" || open -Wn -a Preview /tmp/diff.pdf
```

* and use the new difftool by doing
```
git difftool --tool=pdf
```

Obviously this will only diff pdfs so you might want to only diff a character directory
