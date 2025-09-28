
# MATCH WITH '[ ]'

This module teaches you about [ ] glob.

# FLAG

My Flag ~ pwn.college{U0Jon2j3y7KvRd0oE309Uz30uVz.QXzIDO0wCN0AzNzEzW}


# SOLUTION

```
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{U0Jon2j3y7KvRd0oE309Uz30uVz.QXzIDO0wCN0AzNzEzW}
```


# WHAT I LEARNT

`[]` is a wildcard for some subset of potential characters, specified within the brackets.
For example, `[pwn]` will match the character `p`, `w`, or `n`.


