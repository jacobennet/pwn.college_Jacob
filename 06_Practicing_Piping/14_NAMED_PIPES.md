
# NAMED PIPES

This module teaches you how you can create your own named pipes in system

# FLAG

My flag ~ pwn.college{owEFa0tXSZXMvYaPYX7_GtxinJr.01MzMDOxwCN0AzNzEzW}

# SOLUTION

Terminal 1:

```
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo
You've correctly redirected /challenge/run's stdout to a FIFO at
/tmp/flag_fifo! Here is your flag:
pwn.college{owEFa0tXSZXMvYaPYX7_GtxinJr.01MzMDOxwCN0AzNzEzW}
```

Terminal 2

```
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo!
Bash will now try to open the FIFO for writing, to pass it as the stdout of
/challenge/run. Recall that operations on FIFOs will *block* until both the
read side and the write side is open, so /challenge/run will not actually be
launched until you start reading from the FIFO!
```


# WHAT I LEARNT

You can also create your own _persistent_ named pipes that stick around on the filesystem. They are called **FIFOs**, which stands for First byte In, First byte Out.
You create a FIFO using the `mkfifo` command.




