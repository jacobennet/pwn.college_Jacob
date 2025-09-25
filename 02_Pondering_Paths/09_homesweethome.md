# HOME SWEET HOME


# FLAG

My flag~ pwn.college{03cs2KQXL2Cxc82TNELoqk6GLtK.QXzMDO0wCN0AzNzEzW}

# SOLUTION

```
hacker@paths~home-sweet-home:~$ echo LOOK: ~
LOOK: /home/hacker
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{03cs2KQXL2Cxc82TNELoqk6GLtK.QXzMDO0wCN0AzNzEzW}
```

# What i learnt 

```console
hacker@dojo:~$
```

Bash provides and uses this shorthand because, again, most of your time will be spent in your home directory. Thus, whenever bash sees `~` provided as the start of an argument in a way consistent with a path, it will expand it to your home directory.

echo LOOK: ~ command can be used to know your current directory.
