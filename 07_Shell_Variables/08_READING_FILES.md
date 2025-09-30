
# READING FILES

This challenge demonstrates how to read output of a command into a variable

# FLAG

My flag ~ pwn.college{s-Ftk7QCbt2HlUD5PDmOJ7Y7LMS.QXwIDO0wCN0AzNzEzW}

# SOLUTION

```
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{s-Ftk7QCbt2HlUD5PDmOJ7Y7LMS.QXwIDO0wCN0AzNzEzW}
```

# WHAT I LEARNT

instead of using `cat` to read a file into a variable
you can use the shell's built-in `read` command with input redirection: read VAR < file.