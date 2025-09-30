
# PRINTING EXPORTED VARIABLES

This challenge demonstrates how to print exported variables using env command

# FLAG

My flag ~ pwn.college{AAkGJpx_W3ylsUs9woR-5akLaWX.QX4UTN0wCN0AzNzEzW}

# SOLUTION

```
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=ecf7fe3460b57416845260a40ab9522738531ca067943c8d0c57c626ab341cbe
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{AAkGJpx_W3ylsUs9woR-5akLaWX.QX4UTN0wCN0AzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

# WHAT  I LEARNT

`env` command will print out every exported variable set in your shell.
you can also print variable using echo command.