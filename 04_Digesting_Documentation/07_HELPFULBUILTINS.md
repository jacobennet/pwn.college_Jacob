
# HELPFUL BUILTINS

This challenge teaches you how you can use help command on built in functions

# FLAG

My flag ~ pwn.college{YzabZymfwe_O5BJH5F25KJ-3gbE.QX0ETO0wCN0AzNzEzW}

# SOLUTION

Type in help challenge where challenge is a builtin command in the shell. Then execute challenge --secret VALUE where VALUE is YzabZymf as instructucted.

```
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "YzabZymf".
hacker@man~help-for-builtins:~$ challenge --secret YzabZymf
Correct! Here is your flag!
pwn.college{YzabZymfwe_O5BJH5F25KJ-3gbE.QX0ETO0wCN0AzNzEzW}
```


# WHAT  I LEARNT

You can also use help command on built in commands to know about its arguments.
