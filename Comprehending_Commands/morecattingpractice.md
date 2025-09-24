# More catting practice

# FLAG

My flag ~ pwn.college{wYZPnoOdssbXasKyqyZ9SDTyM_y.QXwITO0wCN0AzNzEzW}


# SOLUTION
```
You cannot use the 'cd' command in this level, and must retrieve the flag by
absolute path. Plus, I hid the flag in a different directory! You can find it
in the file /usr/include/recint/flag. Go cat it out **without** cding into that
directory!
hacker@commands~more-catting-practice:~$ cat /usr/include/recint/flag
pwn.college{wYZPnoOdssbXasKyqyZ9SDTyM_y.QXwITO0wCN0AzNzEzW}

```

# What i learnt
cat command can also have absolute path of the file as arguments. 
You can read contents of file without changing directory.