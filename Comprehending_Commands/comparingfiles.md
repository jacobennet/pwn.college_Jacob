# COMPARING FILES

This module gives information on diff command which compares the contents of two files.

# FLAG
my flag ~ pwn.college{U57JfuXpV_poEkmr2EJ06khr9Dm.01MwMDOxwCN0AzNzEzW}

# SOLUTION

```
hacker@commands~comparing-files:~$ cd /challenge
hacker@commands~comparing-files:/challenge$ diff decoys_only.txt decoys_and_real.txt
3a4
> pwn.college{U57JfuXpV_poEkmr2EJ06khr9Dm.01MwMDOxwCN0AzNzEzW}
```

# WHAT I LEARNT

diff  compares two files line by line and shows you exactly what's different between them.
The output of above tells us that after line 3 in the first file  decoys_only.txt, the second file decoys_and_real.txt has an additional line (`3a4` means "after line 3 of file1, add line 4 of file2").


