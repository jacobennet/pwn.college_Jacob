
# STORING COMMAND OUTPUT

This module demonstrates how to store output of a command into a variable

# FLAG

My Flag ~ pwn.college{wVyJoaxp-lrvCacX25yvQnvB2bz.QX1cDN1wCN0AzNzEzW}

# SOLUTION

Assign output of /challenge/run to variable PWN by $().
then printout PWN using echo

```
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{wVyJoaxp-lrvCacX25yvQnvB2bz.QX1cDN1wCN0AzNzEzW}
```

# WHAT I LEARNT

You can use $() to assign output of a command into a variable

