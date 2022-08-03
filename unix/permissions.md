# Permissions

Use `ls -l` to show all permissions for the current file

Example Output:

```sh
-rw-r--r--    1 root     root           305 Jan  1 01:30 cli
-rwxr-xr-x    1 root     root           183 Jan  1 01:30 run
-rwxr-xr-x    1 root     root            56 Jan  1 01:30 test
```

Say I wanted `cli` to match `run` and `test` in permissions.

You could change this with:
```
$ chmod u=rw,g=rx,o=rx ./cli
```

Alternatively written:
```
$ chmod 655 ./cli
```

Will result in:

```sh
-rwxr-xr-x    1 root     root           305 Jan  1 01:30 cli
```

## Why do we change permissions like this?

We manage permissions based on 3 groups:

- **u** is for **user** *(the file's owner)* permissions
- **g** is for **group** permissions
- **o** is for **other** users

> You'll tend to see permissions and access rights slide from loose to strict as the target becomes less affiliated with the owner (generally)

## How does `u=rw,g=rx,o=rx` become `655`?

The privileges can be represented by one number using the octal system:

- **r** or read is **4**
- **w** or write is  **2**
- **x** or execute is **1**
- no access rights is **0**

If we add these up, you'll notice that any permutation of these privileges results in a unique number! 

- **7** – for **rwx**
- **6** – for **rw**
- **5** – for **rx**
- **4** – for **r**
- **0** - for **none**

Thus we could represent `u=rwx,g=r,o=r` permissions as `744` by concatenating the three numbers to represent the user, group and others in that order.
