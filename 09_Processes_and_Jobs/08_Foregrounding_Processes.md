
# FOREGROUNDING PROCESSES

This challenge teaches you about fg command.

# FLAG

My flag ~ pwn.college{Qe-V4snCAUM4I02b1MydFJP3JP0.QX4QDO0wCN0AzNzEzW}


# SOLUTION 

run /challenge/run then suspend it using ctrl z and rerun it in background by bg /challenge/run.
then run in foreground fg /challenge/run. which will give you the flag

```
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the
background, and *then* foreground it without re-suspending it! You can
background me with Ctrl-Z (and resume me in the background with 'bg') or, if
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg /chalenge/run
bash: bg: /chalenge/run: no such job
hacker@processes~foregrounding-processes:~$ bg /challenge/run
[1]+ /challenge/run &
hacker@processes~foregrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out. After that, resume me into the foreground with 'fg';
I'll wait.

hacker@processes~foregrounding-processes:~$ fg /challenge/run
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{Qe-V4snCAUM4I02b1MydFJP3JP0.QX4QDO0wCN0AzNzEzW}
```


# WHAT I LEARNT

You can foreground a backgrounded process with `fg` just like you foreground a suspended process



