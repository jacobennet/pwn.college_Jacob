
# KILLING PROCESSES

This challenge demonstrates how to kill processes using kill command.

# FLAG

My flag ~ pwn.college{kKwTD9QZ8S2GxgIAn8jwgDAEQyx.QXyQDO0wCN0AzNzEzW}


# SOLUTION

First find the Process id of /challenge/dont_run we can do that by ps -ef and find the pid.
then execute kill command with pid of /challenge/dont_run as argument. then run /challenge/run.

```
hacker@processes~killing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 05:17 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo
root           7       1  0 05:17 ?        00:00:00 /run/dojo/bin/sleep 6h
root         135       1  0 05:17 ?        00:00:00 su -c /challenge/.launcher hacker
hacker       136     135  0 05:17 ?        00:00:00 /challenge/dont_run
hacker       137     136  0 05:17 ?        00:00:00 sleep 6h
hacker       139       0  0 05:17 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run
hacker       145     139  0 05:17 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       163       1  0 05:17 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --int
hacker       167     163  0 05:17 pts/1    00:00:00 /run/dojo/bin/bash --login
hacker       181     145  0 05:19 pts/0    00:00:00 ps -ef
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{kKwTD9QZ8S2GxgIAn8jwgDAEQyx.QXyQDO0wCN0AzNzEzW}
```

# WHAT I LEARNT

Kill command along with PROCESS ID AS ARGUMENT is used to terminate a process.