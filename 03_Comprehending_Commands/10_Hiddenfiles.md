
# HIDDEN FILES

This file teaches you about ls -a command which is used to find hidden files.

# FLAG

My flag ~ pwn.college{sQMe7y76D7e0a-21jTInhp-Sgp3.QXwUDO0wCN0AzNzEzW}

# SOLUTION

Type in ls -a / and read the file  .flag-196072146612825

```
hacker@commands~hidden-files:~$ ls -a /
.   .dockerenv             bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-196072146612825  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:~$ cd /

hacker@commands~hidden-files:/$ cat /.flag-196072146612825
pwn.college{sQMe7y76D7e0a-21jTInhp-Sgp3.QXwUDO0wCN0AzNzEzW}

```

# WHAT I LEARNT

ls -a command can be used to view list of hidden files. which always begins with a dot '.'