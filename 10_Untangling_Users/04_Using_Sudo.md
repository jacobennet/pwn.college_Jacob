
# Using Sudo

This challenge helps you to  understand and use the `sudo` (substitute user, do) command to execute commands with root privileges without needing the root password, and successfully read the flag file.

# FLAG

My flag ~ pwn.college{UYF9ZCAqJ5oIa4bmmpVZOCU59Pb.QX4UDN1wCN0AzNzEzW}


# SOLUTION

Since the flag file is only readable by root, use `sudo` to read it use sudo cat/flag to read the flag.

```
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{UYF9ZCAqJ5oIa4bmmpVZOCU59Pb.QX4UDN1wCN0AzNzEzW}
```


# WHAT I LEARNT

`sudo` has replaced `su` as the modern method for privilege escalation because it allows authorized users to run commands as root without sharing or knowing the root password, relying instead on policy-based authorization defined in `/etc/sudoers` and the user's own password for authentication.
Unlike `su` which requires a password and launches a shell, `sudo` allows authorized users to run specific commands as root based on policies defined in `/etc/sudoers`
