# SSH Config

If you have a static ssh server you're constantly connecting to, it may be a good idea to name it and list it within a ssh configuration file.

To set up an SSH config file for the current user:

## Set up
```
$ touch ~/.ssh/config
```

## Syntax
```
Host server
    HostName server.domain.com
    User username
    Port 4242
    IdentityFile ~/.ssh/id_rsa
```

## Usage
```
$ ssh server
```