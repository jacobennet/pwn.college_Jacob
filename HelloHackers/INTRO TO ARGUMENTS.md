
# Aim

TO  find the flag by passing command along with argument.

# MYFLAG

my **flag** : pwn.college{AXCZTf7zS3qoSycYutCLXXZMZiY.QX4YjM1wCN0AzNzEzW}

# Solution

Type in 'hello hackers' where hello is the command and hackers is a single argument.

# WHAT I LEARNT

[](https://github.com/jacobennet/pwn.college_Jacob/blob/main/HelloHackers.md#what-i-learnt)

When you type a line of text and hit enter, the shell actually parses your input into a command and its arguments. first word is command and subsequent words are arguments

```shell
hacker@paths~program-and-absolute-paths$ hello hackers
pwn.college{AXCZTf7zS3qoSycYutCLXXZMZiY.QX4YjM1wCN0AzNzEzW}
```