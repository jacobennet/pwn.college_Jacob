
# OTHER USERS WITH SU

This challenge teaches you how to switch to other users using su.

# FLAG

My flag ~ pwn.college{U9E0_9Ebo7xfUP2KPXwu8WY03bR.QX2UDN1wCN0AzNzEzW}

# SOLUTION

The challenge instructs you to switch user to zardus. You can do that by su zardus. and type in the password as instructed. Then run /challenge/run.


```
hacker@users~other-users-with-su:~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{U9E0_9Ebo7xfUP2KPXwu8WY03bR.QX2UDN1wCN0AzNzEzW}

```


# WHAT I LEARNT

when u provide a user as argument in su you can switch to that particular user.