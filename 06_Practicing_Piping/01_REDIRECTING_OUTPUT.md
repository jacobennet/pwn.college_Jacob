
# REDIRECTING_OUTPUT

This module demonstrates how you can redirect stdout to files.

# FLAG

My flag ~ pwn.college{Ulc3EQ-C9ys0u-6C3-T6wXlnqpw.QX0YTN0wCN0AzNzEzW}


# SOLUTION

Use `>` character to redirect stdout from PWN TO COLLEGE

```
jacob@DESKTOP-F1CQCK4:~$ ssh -i key hacker@dojo.pwn.college
Connected!
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{Ulc3EQ-C9ys0u-6C3-T6wXlnqpw.QX0YTN0wCN0AzNzEzW}
```

# WHAT I LEARNT

You can use > character to redirect stdout of files ie you can redirect output of a file to another.