
# EXTRACTING SPECIFIC SECTIONS OF TEXT

This challenge demonstrates cut command which is used to extract columns from a text

# FLAG

My flag~ pwn.college{YKnun8KpOECmLlq9mjM5IGUcavd.01NxEzNxwCN0AzNzEzW}

# SOLUTION

First run the /challenge/run program to view the column in which flag is present.
we can see that it is present in column 2. so execute /challenge/run | cut -d " " -f 2 |  tr -d "\n"
here tr -d "\n" is done to remove all new line characters.

```
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run
13849 p
21798 w
20939 n
8425 .
16659 c
22238 o
2446 l
21457 l
31163 e
26791 g
16222 e
15381 {
12624 Y
1802 K
12138 n
31384 u
4819 n
27277 8
29205 K
18606 p
12762 O
6700 E
28714 C
30127 m
21685 L
21518 l
32058 q
32297 9
26708 m
3695 j
8340 M
25292 5
26954 I
9644 G
29388 U
16252 c
5042 a
15689 v
14240 d
30121 .
11026 0
20256 1
28764 N
26224 x
19848 E
9691 z
27652 N
12230 x
232 w
3516 C
25138 N
27164 0
30661 A
13479 z
17961 N
27580 z
1438 E
26130 z
15378 W
24141 }
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{YKnun8KpOECmLlq9mjM5IGUcavd.01NxEzNxwCN0AzNzEzW}
```


# WHAT I LEARNT

cut command is used to extract columns from text. its syntax is cut -d " " -f n
here -d is used to specify the de limiter and -f used to specify which column to extract. where n is the column number.
