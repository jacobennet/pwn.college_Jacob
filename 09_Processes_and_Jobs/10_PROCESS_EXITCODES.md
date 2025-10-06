
# PROCESS EXIT CODES

This challenge teaches you about exit  codes

# FLAG

My flag ~ pwn.college{Qz7Hm6YEbUTj4NrBKvgSyt0cNux.QX5YDO1wCN0AzNzEzW}


# SOLUTION 

store the error code in variable ? using $ symbol. and then print it out using echo. this will give u the error code of /challenge/get-code. now run /challenge/submit-code with the error code as argument which is 77 as shown below.

```
hacker@processes~process-exit-codes:~$ /challenge/get-code $?
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
77
hacker@processes~process-exit-codes:~$ /challenge/submit-code 77
CORRECT! Here is your flag:
pwn.college{Qz7Hm6YEbUTj4NrBKvgSyt0cNux.QX5YDO1wCN0AzNzEzW}
```


# what I learnt

Every shell command, including every program and every builtin, exits with an _exit code_ when it finishes running and terminates.
You can access the exit code of the most recently-terminated command using the special `?` variable.