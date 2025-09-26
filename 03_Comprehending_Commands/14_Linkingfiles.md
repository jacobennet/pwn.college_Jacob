
# LINKING FILES

This challenge teaches you about soft link or symbolic link
# MY FLAG

FLAG ~ pwn.college{Ypig0DYy5APvnpH2IUgCU_HxjYu.QX5ETN1wCN0AzNzEzW}


# SOLUTION

```
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{Ypig0DYy5APvnpH2IUgCU_HxjYu.QX5ETN1wCN0AzNzEzW}
```


# WHAT I LEARNT

symbolic link, or soft link, is a special type of file that serves as a reference or pointer to another file or directory by storing its pathname

In linux -ln s is used to create a symbolic link.

