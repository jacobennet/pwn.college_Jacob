
# GREPPING LIVE OUTPUT

This challenge teaches you how you can avoid  the need to store results to a file by using the `|` (pipe) operator.

# FLAG

My flag ~ pwn.college{QlirMpdfRm-agpCuO2Br0qTS80H.QX5EDO0wCN0AzNzEzW}

# SOLUTION

```
hacker@piping~grepping-live-output:~$ /challenge/run | grep "pwn.college"
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{QlirMpdfRm-agpCuO2Br0qTS80H.QX5EDO0wCN0AzNzEzW}

```


# WHAT I LEARNT

Standard output from the command to the left of the pipe will be connected to (_piped into_) the standard input of the command to the right of the pipe
