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

# Stop!
Don't open any pdf with the macos built in pdf tool Preview! This will break all the fillable form fields making them a **fixed text size!** This means the text will no longer scale as you type, limiting the amount of text you can insert. **Simply opening the pdf with macos preview** is all it takes as the file will be auto saved with all the broken fields. This is very annoying to undo and basically requires you revert back, losing all your work.
