
# MATCHING WITH ?

This challenge teaches you about ? glob.
# FLAG


My flag ~ pwn.college{kynWF33fRaP1POpmAucOgk9Jf1G.QXyIDO0wCN0AzNzEzW}


# SOLUTION


```
This challenge resets your working directory to /home/hacker unless you change
directory properly...
This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{kynWF33fRaP1POpmAucOgk9Jf1G.QXyIDO0wCN0AzNzEzW}
```

# WHAT I LEARNT

When it encounters a `?` character in any argument, the shell will treat it as a **single-character** wildcard.

