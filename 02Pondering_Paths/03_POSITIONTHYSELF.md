# POSITION THY SELF 

The major objective of this module is to explain about navigation through different directories    in Linux filesystem.

# FLAG

My flag ~ pwn.college{0ZzAIzLk5hFlefCIiotOGV9uViz.QX2QTN0wCN0AzNzEzW}

# SOLUTION 

The challenge instructs you to execute /challenge/run.
This will give you an absolute path where you have to rerun the /challenge/run program. You can change directories using command cd.

```
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/include directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /usr/include 
hacker@paths~position-thy-self:/usr/include$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{0ZzAIzLk5hFlefCIiotOGV9uViz.QX2QTN0wCN0AzNzEzW}}

```

# What i learnt

You can change directories using command "cd"





