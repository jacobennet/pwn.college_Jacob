
# LISTING PROCESSES

This challenge teaches you about ps command which lists out all processes

# FLAG

My flag ~ pwn.college{sWQxJF9lgW2OE9DW0OBB1w_QD4n.QX4MDO0wCN0AzNzEzW}


# SOLUTION

Use ps-aux or ps-ef to list  out all of proccess. Find the process which gives flag which is /challenge/20917-run-23162.
run the program to get the flag.

```
hacker@processes~listing-processes:~$ ps -aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.0   1056   640 ?        Ss   05:12   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo
root           7  0.0  0.0 231708  2560 ?        S    05:12   0:00 /run/dojo/bin/sleep 6h
root         132  0.0  0.0   4132  2560 ?        S    05:12   0:00 /challenge/20917-run-23162
root         135  0.0  0.0   2744  1280 ?        S    05:12   0:00 sleep 6h
hacker       146  0.0  0.0  36972 22080 ?        Sl   05:12   0:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --
hacker       150  0.0  0.0 231940  4160 pts/0    Ss+  05:12   0:00 /run/dojo/bin/bash --login
hacker       160  0.0  0.0 231576  3520 pts/1    Ss   05:12   0:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p3
hacker       166  0.0  0.0 231940  4160 pts/1    S    05:12   0:00 /run/dojo/bin/bash --login
hacker       185  0.0  0.0 233600  3840 pts/1    R+   05:14   0:00 ps -aux
hacker@processes~listing-processes:~$ /challenge/20917-run-23162
Yahaha, you found me! Here is your flag:
pwn.college{sWQxJF9lgW2OE9DW0OBB1w_QD4n.QX4MDO0wCN0AzNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').
```


# WHAT I LEARNT

Ps -ef and ps -aux is used to list out all the proccess running in the bash.
There are many commonalities between `ps -ef` and `ps aux`: both display the user (`USER` column), the PID, the TTY, the start time of the process (`STIME`/`START`), the total utilized CPU time (`TIME`), and the command (`CMD`/`COMMAND`). `ps -ef` additionally outputs the _Parent Process ID_ (`PPID`), which is the PID of the process that launched the one in question, while `ps aux` outputs the percentage of total system CPU and Memory that the process is utilizing. Plus, there's a bunch of other stuff we won't get into right now.