# ID

The unix `id` command enables us to find out information about the currently logged in user.

## Usage

To return the current user's system name:
`id -un`

To return the current user's group name:
`id -gn`

## Use Cases

In `~/.bashrc`:

`alias whatami="id -gn"`

This complements `whoami`, _which is essentially `id -un`,_ as a nice way to get the user's group name.