
This module teaches you that an argument can also have an argument.

# FLAG

Myflag ~ pwn.college{8WaDqYTQkX1JitJNZoLKTz6mBOX.QX1ITO0wCN0AzNzEzW}


# SOLUTION

The program asks you to execute /challenge/challenge program which has argument --printfile.
printfile will take file path as argument which will read out the file

```
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{8WaDqYTQkX1JitJNZoLKTz6mBOX.QX1ITO0wCN0AzNzEzW}
```


# WHAT I LEARNT

Arguments can also have arguments in linux.