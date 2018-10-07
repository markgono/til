# SSH Agent

The `ssh-agent` helper command acts as a single sign-on for ssh public key auth connections.

The agent can be started any time a user is logged in, where it will persist for the entire session.

## Usage

### Start the agent

`ssh-agent` will start the agent for the logged in user

### Add a passphrase

`ssh-add` will add a passphrase to the default files.

You can check these with `ssh-add -l` but are usually the following:
- `~/.ssh/id_rsa`
- `~/.ssh/id_dsa`
- `~/.ssh/id_ecdsa`
- `~/.ssh/id_ed25519`
- `~/.ssh/identity`

Otherwise we can pass a filename: 

`ssh-add <key-path>`

## A handy shortcut

To set up an agent and add your passphrase for the default `~/.ssh/id_rsa` key:

In `~/.bashrc`:
```
alias ssh-setup="ssh-agent && ssh-add"
```

Then just use:
```
$ ssh-setup
```

This is always the first command I run when logging in, and saves typing in a passphrase any time a `git pull` or `ssh` is used!