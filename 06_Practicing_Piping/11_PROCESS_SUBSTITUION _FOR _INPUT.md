
# PROCESS SUBSTITUTION FOR INPUT

This challenge teaches you about process substituion for input

# FLAG

My flag ~  pwn.college{w5jFtgwy_UtA2kGQD29tQQis5iZ.0lNwMDOxwCN0AzNzEzW}

# SOLUTION

```
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
32a33
> pwn.college{w5jFtgwy_UtA2kGQD29tQQis5iZ.0lNwMDOxwCN0AzNzEzW}
```

# WHAT I LEARNT

Process substitution in Linux, primarily within Bash and other shells, allows treating the output of a command or commands as if it were a temporary file.
 **Reading from a process:** `<(command)` . This form substitutes the output of `command` as a file-like input. The shell creates a named pipe (a special kind of file) and runs `command` in a subshell, directing its standard output to this pipe.



