# Wget Download and Append

Downloading files with the wget output document (`-O`) set to `-` will print to standard output. Along with `>>` this can append a pre-existing file with the contents.

## Use Case
Use with github/gitignore to generate perfect environment gitignore files, the following will create a .gitignore perfect for Node development on macOS:
```
$ wget http://raw.githubusercontent.com/github/gitignore/master/Node.gitignore http://raw.githubusercontent.com/github/gitignore/master/Global/macOS.gitignore -O - >> .gitignore
```
