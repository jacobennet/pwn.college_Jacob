
# 02 DELETING CHARACTERS

This challenge teaches you about -d argument with tr command which helps u to delete characters in stdoutput and print in stdoutput

# FLAG

My flag ~ pwn.college{M-IW3kqUuiuDtJIvsHjMUWdntIo.0FNxEzNxwCN0AzNzEzW}

# SOLUTION

First run /challenge/run program to see all the flag mixed with some decoy characters. Identify the decoy characters which as we can see is ^%&. Now perform td -d command by /challenge/run | td -d '^%&.' to view the flag

```
hacker@data~deleting-characters:~$ /challenge/run
Your character-stuffed flag:
p^%w^%n^.^%co^%ll^e%g%e^%{^%M^-^%I^%W^%3^%k%q%U%ui^%u%D^%t^J^%I^v^s^H^%j%M^U^W^%d^n^%t%I^%o^.^0^%F^N%xE^z%N^%xw^%C^N%0Az^Nz%E%zW%}^^
hacker@data~deleting-characters:~$ /challenge/run |tr -d '^&%'
Your character-stuffed flag:
pwn.college{M-IW3kqUuiuDtJIvsHjMUWdntIo.0FNxEzNxwCN0AzNzEzW}

```


# WHAT I LEARNT

`tr` can also translate characters to nothing (i.e., _delete_ them). This is done via a `-d` flag and an argument of what characters to delete.