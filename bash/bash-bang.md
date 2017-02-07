# Bash Bang Commands

To save retyping a command, Bash's Bang(`!`) commands allow us to re-run all or part of the previous command.

## Run Last
Enter `!!` to repeat the last command. `!cmd` will also repeat the last command beginning with `cmd`.

## Print Bang
You can also print the resulting bang command before you run it by appending `:p` to the end of your bang.

## Repeat from History
`history` will give you a historical list of all the commands in the current buffer with a numerical identifier. Use `!<command-number>` to rerun a particular command from history.

### Glossary
Here's a list of some common bang commands:

- `!:0` - the name of the previous command
- `!:1` - the first parameter of the previous command
- `!:*` - all the parameters of the previous command
- `!:$` - the last parameter of the previous command
- `!!` - the entire previous command

([via this StackOverflow answer](http://stackoverflow.com/questions/6109225/bash-echoing-the-last-command-run/9502698#9502698))

## Use Case
Re-running with elevated access - `sudo !!` 😎
