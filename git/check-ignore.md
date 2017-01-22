# Git Check Ignore

Sometimes a file is ignored by git and you've no idea why - `git check-ignore --verbose <filename>` will give you the exact location in your .gitignore where the rule ignoring the file is located.

## Backstory
This function was borne out of a [StackOverflow question](http://stackoverflow.com/questions/12144633/which-gitignore-rule-is-ignoring-my-file/12168102#12168102) in which [Adam Spiers](https://github.com/aspiers) completed and patched in a partially implemented version of this feature into the master branch of git!
