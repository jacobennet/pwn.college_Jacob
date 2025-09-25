
# POSITION ELSE WHERE

The major objective of this module is to explain about navigation through different directories  in Linux filesystem.


# FLAG

My flag ~ pwn.college{EMH4MDMOWnuJQIny543wnuVWcUG.QX3QTN0wCN0AzNzEzW}

# SOLUTION 

The challenge instructs you to execute /challenge/run.
This will give you an absolute path where you have to rerun the /challenge/run program. You can change directories using command cd.

```
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:/usr/share/doc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{EMH4MDMOWnuJQIny543wnuVWcUG.QX3QTN0wCN0AzNzEzW}

```

# What I learnt.

You can change directories using command "cd"
