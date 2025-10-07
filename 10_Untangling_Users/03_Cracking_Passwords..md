
# CRACKING PASSWORDS

 This challenge helps you To understand password hashing and cracking by obtaining a leaked `/etc/shadow` file, using John the Ripper to crack the password hash, and then using `su` to switch to the target user account to capture the flag.


# SOLUTION
Use john the ripper the crack the password. 
by john /challenge/shadow-leak. wait for a few minutes. Use john --show /challenge/shadow-leak to view the password.
then switch user to zardus using sb and type in password and run /challenge/run


```
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Created directory: /home/hacker/.john
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:19 100% 2/3 0.05184g/s 301.8p/s 301.8c/s 301.8C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ john --show /challenge/shadow-leak
hacker:NO PASSWORD:20357:0:99999:7:::
zardus:aardvark:20368:0:99999:7:::

2 password hashes cracked, 0 left
hacker@users~cracking-passwords:~$ su zardus
Password:
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{w-HLbADZMGGWxSvWkWc_HeCBQkl.QX3UDN1wCN0AzNzEzW}
zardus@users~cracking-passwords:/home/hacker$

```


# WHAT I LEARNT

password hashes in `/etc/shadow` can be cracked using tools like John the Ripper when leaked