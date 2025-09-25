
# IMPLICIT RELATIVE PATH

The major objective of this challenge is to teach you about implicit relative path.

# FLAG 

my flag ~ pwn.college{ovHlsnsV7TRVhZC9HPHlarBg_z7.QXxUTN0wCN0AzNzEzW} 

# SOLUTION

change directory to  /challenge using cd command and execute run command using relative path '/run'

```
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{ovHlsnsV7TRVhZC9HPHlarBg_z7.QXxUTN0wCN0AzNzEzW}
```


# WHAT I LEARNT

Linux searched the current directory for programs every time you entered a naked path, you could accidentally execute programs in your current directory that happened to have the same names as core system utilities! As a result, the above commands will yield the following error:

```
bash: run: command not found
```






