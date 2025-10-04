
# TRANSLATING CHARACTERS

This module teaches you about -tr command which stands for translates


# FLAG

My flag ~ pwn.college{YdLDFcHjAHJWS9C1DCGgvgve1Sh.01MxEzNxwCN0AzNzEzW}


# SOLUTION

Here the challenge asks u to run challenge/run program which gives flag whose cases are swapped so we swap theese using tr command. "| tr 'A-Za-Z" 'a-zA-Z' we can swap cases.

```
hacker@data~translating-characters:~$ /challenge/run
Your case-swapped flag:
PWN.COLLEGE{yDldfChJahjws9c1dcgGVGVE1sH.01mXeZnXWcn0aZnZeZw}
hacker@data~translating-characters:~$ /challenge/run | tr 'A-Za-z' 'a-zA-Z'
yOUR CASE-SWAPPED FLAG:
pwn.college{YdLDFcHjAHJWS9C1DCGgvgve1Sh.01MxEzNxwCN0AzNzEzW}
```

# WHAT I LEARNT

`tr `  translates characters it receives over standard input and prints them to standard output.
