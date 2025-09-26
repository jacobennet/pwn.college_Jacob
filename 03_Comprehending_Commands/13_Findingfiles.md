
# FINDING FILES

This challenge teaches you about finding files using find command

# FLAG

My flag ~ pwn.college{cwKMqLDXbuDYwfIq2UWVygCctjd.QXyMDO0wCN0AzNzEzW}

# SOLUTION 

```
hacker@commands~finding-files:~$ find / -name flag
find: ‘/tmp/tmp.TpSOPGOVKK’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/mysql-files’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/mysql’: Permission denied
find: ‘/var/lib/mysql-keyring’: Permission denied
find: ‘/var/lib/php/sessions’: Permission denied
find: ‘/var/log/private’: Permission denied
find: ‘/var/log/apache2’: Permission denied
find: ‘/var/log/mysql’: Permission denied
find: ‘/run/mysqld’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/root’: Permission denied
/opt/linux/linux-5.4/drivers/infiniband/ulp/flag
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
^C
hacker@commands~finding-files:~$ cat /opt/linux/linux-5.4/drivers/infiniband/ulp/flag
pwn.college{cwKMqLDXbuDYwfIq2UWVygCctjd.QXyMDO0wCN0AzNzEzW}

```


# WHAT I LEARNT

find / -name flag is used to find  names of all file starting with flag. You can search for any file in linux using flag command.