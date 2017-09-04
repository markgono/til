# Recover a Dropped Git Stash

If you accidentally drop a git stash using `git stash drop`, you can recover it using the ref output from the command:

```
$ git stash drop
Dropped refs/stash@{0} (be4d35e64561cff241a5cbd22805e6be880c041e)
```

To recover that stash, run:
```
$ git stash apply be4d35e
```
