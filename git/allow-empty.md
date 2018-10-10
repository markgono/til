# Allow Empty Git Commit

The `git commit` command guards against empty commits, but if you need it for testing a pipeline or triggering a deployment, you can pass the `--allow-empty` flag to override the check.

## Usage
```
$ git commit --allow-empty -m "Deployment trigger"
```