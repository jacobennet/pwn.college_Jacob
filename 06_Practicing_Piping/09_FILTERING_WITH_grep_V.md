
# FILTERING WITH GREP_V

This challenge teaches you about -v argument of grep

# FLAG

My flag ~ pwn.college{QxF1YFRmMxHK3BfzXxKx_5I_Zk3.0FOxEzNxwCN0AzNzEzW}

# SOLUTION

```
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v 'DECOY'
pwn.college{QxF1YFRmMxHK3BfzXxKx_5I_Zk3.0FOxEzNxwCN0AzNzEzW}
```

# WHAT I LEARNT
`rep -v` shows lines that do NOT match a pattern

