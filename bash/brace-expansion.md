# Brace Expansion

Bash can save you time when typing repeated strings by 'generating' strings for you, when given a range (`{1..10}`) or list of strings (`{a,b,c}`). It'll take the preambles and postscripts (characters immediately before and after the braces) and generate a set of strings using the brace contents.

## Examples
Running `echo {1..5}` will result in `1 2 3 4 5`

Running `echo a{1,5,9}b` will result in `a1b a5b a9b`

### Notes
Braces can be combined, so `echo {A,B,C}{0,1,2}` will result in `A0 A1 A2 B0 B1 B2 C0 C1 C2` 

They can also be nested, so `echo {{0..9},{A..F}}` will result in `0 1 2 3 4 5 6 7 8 9 A B C D E F`

## Use Cases
Downloading multiple files with wget:
```
wget http://raw.githubusercontent.com/github/gitignore/master/{Global/macOS,Node}.gitignore -O - >> .gitignore
```

Initializing files:
```
touch {index,app}.js
```
