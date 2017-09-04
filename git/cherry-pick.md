# Git Cherry-Pick

Made a commit on the wrong branch? Use `git log` to get the commit reference:
```
$ git log --graph --oneline
* dfa74cb (HEAD -> develop) Git - Cherry-Pick
* 91f1f59 (master) Git - Recover Dropped Stash
```

You can switch to the branch, and then use `cherry-pick` to apply the commit: 
```
$ git checkout master
$ git cherry-pick dfa74cb
```

Which results in:
```
$ git log --graph --oneline
* 3301505 (HEAD -> master) Git - Cherry-Pick
* 91f1f59 Git - Recover Dropped Stash
```

If you don't want to commit the changes straight away, use `git cherry-pick -n <ref>` to just stage the changes instead.
