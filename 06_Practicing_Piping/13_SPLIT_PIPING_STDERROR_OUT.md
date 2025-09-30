
# SPLIT PIPING STDERROR AND OUTPUT

This module teaches you how to redirect stdout to one program and stderr to another.

# FLAG

My flag ~ pwn.college{g07-DaHdeCpOxGiG-Bp_gNJHIBV.QXxQDM2wCN0AzNzEzW


# SOLUTION

By doing   > >(command) we are transfering stdoutput of /challenge/hack to temporary pipe file of /challenge/planet and 2> >(command) we are trasnfering error to temporary file in /challenge/the


```
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >(/challenge/planet) 2> >(/challenge/the)
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{g07-DaHdeCpOxGiG-Bp_gNJHIBV.QXxQDM2wCN0AzNzEzW}

```

