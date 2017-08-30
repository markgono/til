# PBCopy

Using `pbcopy` we can interact with the clipboard and copy some content. `pbpaste` allows us to do the reverse!

## Use Cases
Copy your SSH key to the clipboard:
```
pbcopy < ~/.ssh/id_rsa.pub
```

Pipe the contents of our .gitignore to the clipboard:
```
cat .gitignore | pbcopy
```