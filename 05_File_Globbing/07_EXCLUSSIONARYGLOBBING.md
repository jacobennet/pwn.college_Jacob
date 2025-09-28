
# EXCLUSIONARY GLOBBING

This module  demonstrates how if ! is first character in [] it excludes all characters inside the [  ]
globe.
# FLAG 

My flag ~ pwn.college{kzpkwh4Io3GEwhBxAo_B6Ld2U04.QX2IDO0wCN0AzNzEzW}

# SOLUTION

```
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{kzpkwh4Io3GEwhBxAo_B6Ld2U04.QX2IDO0wCN0AzNzEzW}
```

# WHAT I LEARNT

f the first character in the brackets is a `!` or (in newer versions of bash) a `^`, the glob inverts, and that bracket instance matches characters that _aren't_ listed.


