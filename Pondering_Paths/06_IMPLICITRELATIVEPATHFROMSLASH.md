
# IMPLICIT RELATIVE PATH FROM /

The major objective of  this challenge  is to bring about the concept of relative path
# FLAG

My flag ~ pwn.college{sRdvEjp0Sa2hIrvDqX1MTypc8YJ.QX5QTN0wCN0AzNzEzW} 

# SOLUTION

run `/challenge/run` using a relative path while having a current working directory of `/`

``
```

hacker@paths~implicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{sRdvEjp0Sa2hIrvDqX1MTypc8YJ.QX5QTN0wCN0AzNzEzW} 

```
# What i learnt.

A relative path is any path that does not start at root.
A relative path is interpreted relative to your current working directory.
Your cwd is the directory that your prompt is currently located at.
