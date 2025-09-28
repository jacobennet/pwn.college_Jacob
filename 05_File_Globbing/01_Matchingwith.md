
# MATCHING WITH *

This module teaches you about first glob which is  `*` .


# FLAG 

My flag ~ pwn.college{c5-Vo1DUV78tMmrXT9IjimNJgOq.QXxIDO0wCN0AzNzEzW}

# SOLUTION

Type in cd /ch* to move to challenge directory and then execute /challenge/run command

```
This challenge resets your working directory to /home/hacker unless you change
directory properly...
This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{c5-Vo1DUV78tMmrXT9IjimNJgOq.QXxIDO0wCN0AzNzEzW}
```

# WHAT I LEARNT

When it encounters a `*` character in any argument, the shell will treat it as a "wildcard" and try to replace that argument with any files that match the pattern.