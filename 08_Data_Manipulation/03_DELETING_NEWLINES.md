
# DELETING NEW LINES

This challenge demonstrates how to remove new line characters

# FLAG

My flag ~ pwn.college{wJw4iIP0yCRgJ639Y3uxaYNG3fi.0VNxEzNxwCN0AzNzEzW}

# SOLUTION

As instructed in module \n is used to represent new line character. so we remove all new line character by executing /challenge/run | tr -d '\n'

```
hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"
Your line-split flag: pwn.college{wJw4iIP0yCRgJ639Y3uxaYNG3fi.0VNxEzNxwCN0AzNzEzW}hacker@data~deleting-newlines:~$
```

# WHAT I LEARNT

\n are escape sequences which cant be directly typed. hence its represented using a back slash \ .