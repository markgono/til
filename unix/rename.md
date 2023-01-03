# Rename

The rename command allows some easy filename replacements. 

## Example

Renaming a React component named `Alert` to `AlertMessage` in the following structure:

```sh
$ ls 
index.jsx  Alert.jsx  Alert.module.scss  Alert.md
```

We'd run rename on the current directory 

```sh
$ rename 's/Alert/AlertMessage/' ./*
$ ls 
index.jsx  AlertMessage.jsx  AlertMessage.module.scss  AlertMessage.md
```