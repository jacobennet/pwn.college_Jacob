
# SUSPENDING PROCCESES

This challenge demonstrates about Ctrl+Z which used to suspend all running processes

# FLAG

 My flag ~ pwn.college{chKk_CSWs8OwFbpP-GCoKEgl5bT.QX1QDO0wCN0AzNzEzW}

# SOLUTION

as instructed first run /challenge/run program and then suspend it. after that ctrl+z to suspend it. then rerun /challenge/run program to run the copy of the proccess to obtain the flag


```
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         161     141  0 05:35 pts/0    00:00:00 bash /challenge/run
root         163     161  0 05:35 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         161     141  0 05:35 pts/0    00:00:00 bash /challenge/run
root         168     141  0 05:35 pts/0    00:00:00 bash /challenge/run
root         170     168  0 05:35 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{chKk_CSWs8OwFbpP-GCoKEgl5bT.QX1QDO0wCN0AzNzEzW}
```

# WHAT I LEARNT

You can _suspend_ processes to the background with `Ctrl-Z`