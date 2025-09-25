
# EXPLICIT RELATIVE PATH FROM /

This module teaches us about explicit relative paths.

# FLAG

My flag ~ pwn.college{U0SSV-Mg_qckBCrcbThsrjdROIP.QXwUTN0wCN0AzNzEzW}

# SOLUTION 

Change your directory to '/' using cd command. And then execute ./challenge/run to obtain your flag.

```
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{U0SSV-Mg_qckBCrcbThsrjdROIP.QXwUTN0wCN0AzNzEzW}


```


# What i learnt 

In most operating systems, including Linux, every directory has two implicit entries that you can reference in paths: `.` and `..` 




