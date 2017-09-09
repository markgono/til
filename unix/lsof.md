# LSOF

The `lsof` command is to list open files

You can use it to:
- List all process which has opened a file:
  ```
  $ lsof ./cron/script.sh
  ```
- List all opened files by a user:
  ```
  $ lsof -u markgono
  ```
- List all opened files by port:
  ```
  $ lsof -i:3000
  ```

Using this information:
```
$ lsof -i:8000
COMMAND  PID     USER   FD   TYPE             DEVICE SIZE/OFF NODE NAME
node    8528 markgono   51u  IPv4 0x78fb118ce8927df5      0t0  TCP localhost:irdmi (LISTEN)
```

You can do something with the process information, like:
- List all files which have been opened by that process:
  ```
  $ lsof ./script.sh
  …
  node    8532 markgono   21r     CHR                3,2      0t0        311 /dev/null
  node    8532 markgono   22u     CHR               16,1      0t0        653 /dev/ttys001
  node    8532 markgono   23u     CHR               16,1      0t0        653 /dev/ttys001
  ```
- Kill the process:
  ```
  $ kill -9 8528
  ```