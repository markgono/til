# Print Latest File Containing String

Grepping the latest file containing a string using the (`-l`) flag, then take the last item returned using `tail -1`, you can get the latest filename of a file containing any given string. When wrapped in This can be passed along to `less`, `cat` or `vim` to instantly read the file containing the last occurence of any given string.

## Use Cases
Get me the last log with the string "Error" in it:
```
$ less $(grep "Error" -l *log | tail -1)
```

Get me the last log with the string "Error" and jump to the first iteration:
```
$ x="Error"; less -p$x $(grep $x -l *log | tail -1)
```
Tip: use `n` and `N` to page through occurrences. I find this much more useful than grepping alone!
