# Looping in Bash

You can use bash's [brace expansion](./brace-expansion) command to create a sequence with a `for` loop to repeat a command _n_ times:
```
for i in {1..100}; do command; done;
```
This iterates a hundred times executing `command` each time.

We can use this structure in multiple ways:
- `command` can be a pipe or any sequence of commands separated by `;` or `&&`
- `{1..100}` can be any range we desire.

We can also use `$i` between `do` and `done` to know which iteration we are currently in

## Use Case

I commonly use this to drop a bunch of stashes. 
_Just remember:_ `git stash` _works as a stack, so you only need to drop the same number every time._

```
for i in {1..13}; do git stash drop 1; done
```

This will drop 13 stashes, excluding your latest one!