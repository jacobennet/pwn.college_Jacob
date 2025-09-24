
# POSITION YET ELSE WHERE

The major objective of this module is to explain about navigation through different directories    in Linux filesystem.

# FLAG

My flag ~ pwn.college{E19aON7bVVBkEibBZ4ech_QhuGT.QX4QTN0wCN0AzNzEzW} 

# SOLUTION 

The challenge instructs you to execute /challenge/run.
This will give you an absolute path where you have to rerun the /challenge/run program. You can change directories using command cd.


```
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /var directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /var
hacker@paths~position-yet-elsewhere:/var$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag
pwn.college{E19aON7bVVBkEibBZ4ech_QhuGT.QX4QTN0wCN0AzNzEzW}


```

# What i learnt

You can change directories using command "cd"
