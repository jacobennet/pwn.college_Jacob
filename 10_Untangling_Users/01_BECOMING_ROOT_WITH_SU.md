# BECOMING ROOT WITH SU

This module helps you to understand and use the `su` (substitute user) command to elevate privileges to root access by providing the correct root password, and successfully read the flag file.

# FLAG

My flag ~pwn.college{UJVLK0CWWo9t1P3l5UhorO9XYIZ.QX1UDN1wCN0AzNzEzW}

# SOLUTION

su or setuid binary is a commandallows users to switch to another user account (typically root). Run the su command to attempt to become root.
When prompted, enter the root password provided in the challenge
then read the flag by cat flag/

```
hacker@users~becoming-root-with-su:~$ su
Password:
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{UJVLK0CWWo9t1P3l5UhorO9XYIZ.QX1UDN1wCN0AzNzEzW}
root@users~becoming-root-with-su:/home/hacker#

```


# WHAT I LEARNT

su command is used to switch users.


