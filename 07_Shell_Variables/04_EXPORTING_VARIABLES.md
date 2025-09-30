
# EXPORTING VARIABLES

This challenge demonstrates how to export variables so that it isnt restricted within its local shell.

# FLAG

My flag ~ pwn.college{8s3Ip4yQxDssv__OOMNXYqDY_DC.QXyYTN0wCN0AzNzEzW}

# SOLUTION

```
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{8s3Ip4yQxDssv__OOMNXYqDY_DC.QXyYTN0wCN0AzNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```

# WHAT I LEARNT

You can export a variable using export  command.
