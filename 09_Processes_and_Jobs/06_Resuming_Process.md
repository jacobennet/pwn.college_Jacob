
# RESUMING PROCESSS

This module teaches you about fg command which is used to resume a suspended process

# FLAG

My flag ~ pwn.college{4I_9dWz_-qavpEILCYQvCC8gE_S.QX2QDO0wCN0AzNzEzW}

# SOLUTION

Run /challenge/run and suspend it using ctrl Z . then resume it by running it in foreground by fg /challenge/run. 

```
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg /challenge/run
/challenge/run
I'm back! Here's your flag:
pwn.college{4I_9dWz_-qavpEILCYQvCC8gE_S.QX2QDO0wCN0AzNzEzW}
Don't forget to press Enter to quit me!

Goodbye!

```


# WHAT I LEARNT

You can resume suspended process using fg command.