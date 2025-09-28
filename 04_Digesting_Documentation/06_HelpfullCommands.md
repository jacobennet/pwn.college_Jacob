# HELPFUL COMMANDS

This challenge teaches you about help  argument which can be either --help or --h depending on program


# FLAG

My flag ~ pwn.college{kNjUkd1QFnniNYcEQRHznmYFbP4.QX3IDO0wCN0AzNzEzW}


# SOLUTION

Type in /challenge/challenge --help which gives u information about various arguments of /challenge/challenge.
execute /challenge/challenge  -p to print value of number which is argument for /challenge/challenge -g which gives you the flag


```
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 143
hacker@man~helpful-programs:~$ /challenge/challenge -g 143
Correct usage! Your flag: pwn.college{kNjUkd1QFnniNYcEQRHznmYFbP4.QX3IDO0wCN0AzNzEzW}
```


# WHAT I LEARNT

If a command doesnt have a manual u can use --help or -h or -? as argument to know more about the arguments of the command.