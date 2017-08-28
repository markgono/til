# Find

The unix `find` command can be used to locate files across the filesystem. 

## Usage

Commonly used as:
`find <path> -name <filename>`

To find the current user's run command files:
`find ~ -maxdepth 1 -name *rc`