# WRITING TO MULTIPLE PROGRAMS

This challenge teaches you that you  can also use process substitution for _writing_ to commands.

# FLAG

My flag ~  pwn.college{8wLVJxQBWozz2a-ORFD81RPUDIb.QXwgDN1wCN0AzNzEzW}


# SOLUTION

```
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and
/challenge/planet. Don't try to copy-paste it; it changes too fast.
2875745691605411477
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{8wLVJxQBWozz2a-ORFD81RPUDIb.QXwgDN1wCN0AzNzEzW}
```

# WHAT  I LEARNT

 We can split and duplicate data streams in Linux pipelines using tee (to copy data to multiple destinations) and **process substitution `>()`** (to redirect output directly into commands as if they were files).

