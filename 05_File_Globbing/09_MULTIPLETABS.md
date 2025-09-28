
# MULTIPLE OPTIONS FOR TAB

This challenge demonstrates situation if there are multiple options after tab completetion
# FLAG

My flag ~ pwn.college{gfKHoKriZpjwNcVgoAjTFNn6vpV.0lN0EzNxwCN0AzNzEzW}

# SOLUTION

```
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwn
pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter
pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{gfKHoKriZpjwNcVgoAjTFNn6vpV.0lN0EzNxwCN0AzNzEzW}
```

# WHAT I LEARNT

By default `bash` will auto-expand until the first point when there are multiple options.When you hit tab a _second_ time, it'll print out those options.

