


# FLAG

 MY FLAG ~ pwn.college{Q939hwk1rVgTel-xAQxIDflJOTL.0FNzMDOxwCN0AzNzEzW}

# SOLUTION

First run ps-ef command to list out all the processes. Here we found pid of /challenge/decoy which is hogging the critical resource ie /tmp/flag_fifo_hacker. Now run /challenge/run and cat /tmp/flag_fifo_hacker to get the flag. we can see alot of decoy flags because ux pipes are _buffered_: conceptually, they have a sort of length through which data flows, and you might kill the decoy process while data is in the pipe. you can obtain the actual flag by waiting a second and rerunning /challenge/run.

```
hacker@processes~killing-misbehaving-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 05:30 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-i
root           7       1  0 05:30 ?        00:00:00 /run/dojo/bin/sleep 6h
root         137       1  0 05:30 ?        00:00:00 /bin/bash /challenge/.init
root         138       1  0 05:30 ?        00:00:00 /bin/bash /challenge/.init
root         139       1  0 05:30 ?        00:00:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker
root         140     138  0 05:30 ?        00:00:00 sleep 6h
root         141     137  0 05:30 ?        00:00:00 sleep 6h
hacker       142     139  0 05:30 ?        00:00:00 /usr/bin/python /challenge/decoy
hacker       153       1  0 05:30 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --po
hacker       156       0  0 05:30 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/
hacker       163     156  0 05:30 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       172     153  0 05:30 pts/1    00:00:00 /run/dojo/bin/bash --login
hacker       182     163  0 05:31 pts/0    00:00:00 ps -ef
hacker@processes~killing-misbehaving-processes:~$ kill 142
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
^C
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{pJh-iFyvezX5yU2y8AmBA4CYDaEDhPYzFb3hNOxtMkdTsWA}
pwn.college{fq.zMqUjN-aeDubR33FZiK.lOVAcIZFTTGJndkKrP4Ww3U4}
pwn.college{-GZkLf5E6FW5xymaUGDEtUTVejGo07xrX0wdqLDChGc1ciU}
pwn.college{IescQ9yIv9T4AgattalUu6AyQ5-g3hTqTqN2FSBbC..fHFd}
pwn.college{MDWAOXz0DVKivDGT6hvEoHFXiE0hM39DNCsJdKpRzX4BEvu}
pwn.college{86SYJf--6QrsbDkYyQeQ-nqfLqcpkMqfMd-q5qf4Lkcyyz6}
pwn.college{Gx1L03w8AZWlui0H5OpS3k3ZV-8nPo6MK82Opog30AkipXN}
pwn.college{kRcoSIA2yz-z08hxyzhMFrHNvxHCZUZx1Zn2SIV-4aIiRKv}
pwn.college{mJNkEk.bp0y009W-2OGeZ0d4HtRjPTJaVhH.N7GcrMZCOq5}
pwn.college{9fGOmTJfG9IDS3F7L9QkWX0MuuzowGoUDISRD4.IlXZjgKX}
pwn.college{r099RL10CRPqad2gvmYvJS5Yy0F1uA6DGyVBRqgH--cb1H7}
pwn.college{7hsX-QcU5-aDknwYr6ssWketTqM5.jmActUkR4rdybaOx2U}
pwn.college{GgmuKuF0dnj262jx1HvTZmoNtzD4jkAb00wGOCmxqbo1epL}
pwn.college{hpXs2BTrGUW54o04UbAIsrhuw0xi7gynyP681NF-dGCyEAz}
pwn.college{dFZ0SP2ekicObxkrnirMFKxScSXFJKGbxnXIonVjQ4lq8Ak}
pwn.college{Xp-7Fi7ziUFoU3cGeZAVOEQlFAIry9vhkbjn9qh8CuMiyht}
pwn.college{yyLcyRpgFVhKwezg4dDl0.dWs1iT7RhvQzevYVMkqzAuq5k}
pwn.college{VYlhLelme6ApjVgg0LMkWSICmd48xSV1ApkVMqhvzEGsdGS}
pwn.college{d5AtutNbqeDhlpDjq.oe87jZlW3jiG9-nNOGjYruuINFyOh}
pwn.college{sQ-mb1ts3hnd7eukYEDOqlWoNmL5.W7SMhClGYmP3Wdk2Im}
pwn.college{8TaNkFAO4D-oaUqrsncwIWF84mISr8fRDRGKBCsgVEQsVRq}
pwn.college{CA7h0gB4NnVc9cEo3pStwj6Oe3y6.NiEC.lx5rdDgC0-HVE}
pwn.college{YYWmXCMGbkazViGa31BWbt7HNWQOjnwxHDZyu1FT10GxLs6}
pwn.college{b6RwoyDIKL-xuqI6Pf80-Jdl6Rnl0pGH.u2mPz0JLFORt3o}
pwn.college{8y13h553bEvNe2tjSfpr8g0VT9Tycr6-rPTdHCUzsRc54vU}
pwn.college{dyrtzKdbJQ3R7nbm4CH3nM7Kl7RYtj2XCUtuI9CTtE8KA6Q}
pwn.college{UhiTW8BsvaVpOPDlP8UWDgc8CATPNWFF97tQy.zfcNtp8yT}
pwn.college{9f3nPj2WB6n5qBfZc-0pS7Y5Rb82t3psptAKHRkqoKKB8YO}
pwn.college{7jVaJsbxM1D3AEMngJb91EhwbgcTmpCn-0gqu93ETtE-6Uu}
pwn.college{IG-S6cmRq.oePe9SmWYV.LsrMLaksDmJXfeKxX5zjzLFqjg}
pwn.college{UujOkLmGah4QangLRH0LYhr-vFpD5kif8ZdCZgUfjjhKjdw}
pwn.college{M5AWETd6hrYpUbrOvzxPKBEpSWrfzUitb0CPnVspHyfmi7F}
pwn.college{Znr56QcdFaZq.2K0cLQkr2Bvkagp6Zc2fQcIVtrBiqp1Oxs}
pwn.college{1Cqb7pZC4UC6OQ8P.36E2nQ4IQfO9mKSqLuKwcF8ufwB8x1}
pwn.college{6R8efG1zUMymmc-BVS1csJ7OGSuxyGhKl0QOnxZFUuojD5F}
pwn.college{vimVDEkx9xpNkE0HU-cdXBcCbm.8oMDzjET1N3edm9UpvKd}
pwn.college{Zn1xBuHexH6Vcnk1HzSBkXIYkoLfKkovL0-xU-fkzoRTrZj}
pwn.college{TizEEddSoVoHxgRJbnT.fiSo3ud4jHhvBApXDczAOjPa9qZ}
pwn.college{B3yUFyp4IkM.-ubfmH950pH9FnYce.bXNIoa1KQFkG15WLw}
pwn.college{bxWX3zkDuDrEUOcZ1663-3fJlhoWhfeXQKt.28q96dKUib3}
pwn.college{UYew1AolIlXyZmuiMhKpBNRc0d9E3I894ZB6FJ6LEJa3wfB}
pwn.college{YOK.76asTXmWRaFM7vcDRghrwdI361r1NBGuZDZ7JLlfa0U}
pwn.college{L8jc70iddm6YwwItutBOwLl7Ninw2BiAov5r9ptOpGL0Jrr}
pwn.college{7YzzqVfCxNIH.jYj.WlFkosqDslpvh7y3gY4NoE3m46rVEQ}
pwn.college{VLAmSuuwxQ.3HeB7f.hcPZgh-KthIm.gh9n9OEEWlXHoMqp}
pwn.college{auOEbh4RJ6zp-HbQM74LUn9bdyhYhBfKl9CqQOnnn7GNJ9T}
pwn.college{I6ibkytOKnzeC2cyGXu9gxZYidzBWkOil4I1yi7BNGHt6Iy}
pwn.college{7uRFyVpNhZK-5AfE801nQQtlQ2L89htV069g3h1g5JbSAVe}
pwn.college{1559LCGrjsFhQFtn8UZEyNnnhvj5.zkpJuXC5Bb1WnyxnUT}
pwn.college{O0clsZZmZbVPzKjP8KU0lmWQxEq49bHXLBsj23Lt9nA5Z.G}
pwn.college{H.z-7zhkXSYA.KsLuxOouQZtgRUEyw9K-uaXmtyyaK5zWAH}
pwn.college{ZfwdpWdU0E1iXpN4Yucb2.BWoROYBYsvQoEr6Hl-wFGtL14}
pwn.college{ZLctpqBa9AIxb0TGy4tseaEd4VtpPpu556B83JrAoZTX1lc}
pwn.college{uIGS5PYvNCufk9fqVc93sNk8gjLBYEw6v3iH387c0nbAnzw}
pwn.college{dtkZ-pVuuoEdTEFAjhYdGTcwokj2jMn5y6RuEBrDx9kHvgr}
pwn.college{Ow984jF6eZuQ-lczpJdnRGCO3bAkgEUg1-KiLpNz8x6a1gD}
pwn.college{Hc7lPJQ7Ptc68-XAgNhQIHBSu-uAZcgcUhyFVZlgQq0bB5k}
pwn.college{c0Nn43WTl97BPBzD6S9CCN2Qbu6IFf9Slmef99rbh4AQApN}
pwn.college{EbTqDYKRQ3bLH.g.i1Zf91Yv2DCosWF9J8CRm2yZ52rxyaC}
pwn.college{X9eZ7U2DfXBrCUKvC52pbjrxzuLgMl27okYBgRE3D0.Domc}
pwn.college{6NQ0FyVs0ak4cBFK68cE2k87uhgmPfJ9r0mE0KwGU5IIhCE}
pwn.college{c.A9swEQdh9zkiDMvSmC.TuboKPPA512XCQIN.qMEsyxwB9}
pwn.college{Q02FaTr3M4a7MlOh4V1UEqYBP7WPfTZQajs6w0HCC757KXT}
pwn.college{WajNDRLvLGxWgt5bQJKPm66JLYssu3d89cKuwaaSEVTWCx3}
pwn.college{72NzuzJkwT2Vqn0jwOtizAz5Y5Ig2.76QFJ8b3wpx1wDBeM}
pwn.college{26lTpt0rliPGzbNa-WcsDkdQRC0UEtw2oF02knlHhpVuudl}
pwn.college{uTEv9SnhpW1Lyezx-59WovMld6oSPlmpdOIiJ6Q16ontQpF}
pwn.college{I0IXx-ORMJJD83vWuVvuvwm0ExUz.c7O9kw9XqFgkdCO31p}
pwn.college{.gac1GjX53Ws6tOgkKgOvZm3NPvMVXuNnfUAetAK-fqQci-}
pwn.college{lC6lMzFLheMLA2M4SIX0XuQb-jMlYbz3RjZGW4hawQxz8sj}
pwn.college{yrK14LJxIz8PvWhrPn7.peX5RBZ8fcVo8YuSGnzQ-bKLxp7}
pwn.college{g4uhUjfM-j2PSYxdD8nA3OxoskDcBnoR2IbjTayWVAEeBKf}
pwn.college{J7os6Iyg2GnyS0SyH9r3WO.x7ri67uCxkGI9fP50DSjBuwt}
pwn.college{yL2gxB0HD0GGgDDlMoMUqolvlwzfxBzPaqSCg7jr8xiBmsH}
pwn.college{C5rjW5xYgdfU0VhcEkDwP9nVqvpcpxxo9n5UyYPChekS14k}
pwn.college{OVaRS4XeXbuJATWvnaq8rU9w-cqgTzsQLpKdK-yi8dXOP1-}
pwn.college{MPjH8K2FwgzSjzDArL1T5ID6Q4O02qzJWOc7eaWaTXJlYzQ}
pwn.college{KFzVNHoRMLfykJxIiOGFOildEnwXHJf9HvwILZyRFA36MeA}
pwn.college{JuDV9FdoLFYHNg7SEknxQUulv5Hz91N6xnmzecAD-CVM4bk}
pwn.college{SiG-dcMYpojxeLmDoLHamjrrTzvSNiW29tc-IQ0yBD1DDfd}
pwn.college{Nh7XTTOD8jfil5Fd0jJdDisZQYbOCg9gAkkJKX9nw34XAGe}
pwn.college{KMFlBubl3CHh88EbW3HgdXVioHOg4fBqNHRyGC9HRrbbdr.}
pwn.college{aUfVChy3QBe.PAgottNJFgkYtMPq9g2FRzxPSszrMG5F1CL}
pwn.college{Qr4g69maevv1jEDa60ccfJ1PjNhTaxZPe8o.5EawhjmVBRc}
pwn.college{ZxXqKrD.0pUcES65lnHNX04E031COJecC-k23p3bn9zi5E0}
pwn.college{SzjqhYUj2-e9lQklVcTy2FaLihF4JOfw2r3rQMKzS1zDqTy}
pwn.college{rztMVySQHULAq8TgjApk8e6.OCfhvoH9Kb9zRM8D6uhmVru}
pwn.college{7x7XMZwXDl.DnKQDbxZXoCo79Hg-5IAUwN1PRHexOZqEL3n}
pwn.college{jKQtX-geewnA-YB5i7hojNI4PSWndH-8Ql444a89Dy-XCid}
pwn.college{zxAF5vi788lD085XAkhidjAdwrT77.5dFw.9DTgf0mQarJ8}
pwn.college{8OguNC5jO3bnXESOkLzur.iUlSjOnY3RSFiUCC3I.ocvRsj}
pwn.college{u0J1xazBXaF75F0GHNqo.SblkGGNoSUjp-IDqMiLnycRgOg}
pwn.college{86sPhbCp9BlHquE87FK4KrCiq2l.VZ5qnoENEaCXS03rCCk}
pwn.college{dphgCqXIz4kpS0XAAPXHjEb3IwYDdebeTl2VZ5.AUthjjm8}
pwn.college{sOjxIoGSUiizz.IyMSwylghs9FsDXNxuAH9Kc70b1JtYvxR}
pwn.college{iIqFDJ374pOjBZDVnSGbOXYLm6pWjnMX-uxFIHS9P7wGZ4r}
pwn.college{lve-oGMoDL8qJ1sYf45SphGSJFWk6tKhq72gSiUB1rao6ED}
pwn.college{6KJhUzgTuNpCbJS9yMKc7rz75RELQr81Vp3-y9umY2-B7g3}
pwn.college{dZAKRlPoJtFXv0Kx3-4iTJDDg93UgQdn5aZm1c5GGr-EjS4}
pwn.college{SEXELF-SUcCyfGpCQWBMMQhPmjVf0dI.fqBaMytuPmM8B8K}
pwn.college{QjQIlh1gv1I.Ak85IGSHS2yLqrzZgrdKxQ8qCU86qS3tuAK}
pwn.college{OclV64.B99VQZqegZk8AWpRX806ZwQAH8QbjADbx8GJCPPA}
pwn.college{nvG4Z9GhO2GbQwg5ZUhe3JoqxNJZyLL1J67uvXtFXoaZpTR}
pwn.college{IMfN55pI0MclcdMPBp8bOfeBGtlj.S6BsQKthKA0HdwQIj-}
pwn.college{9kRgu89lNPIcIT9hVorrCsvJxIcl-4eWeXW49z6iNUsiG3b}
pwn.college{EKbU3MG9XswDYDAJ5GxwTx5Tp1tXzHzK30X-7QW07hj4ZtQ}
pwn.college{pGWJQhAZmWW2tR1kWl6TfTGHv0SzIW.-h0p-hXcPVFigDcQ}
pwn.college{mlghHnLKJAr6ZSSkucRAYwBTKcWAzxb5Gg8JMpw.55Xnhr7}
pwn.college{yRDhkeAIV.GhusVwiKdMrfdWLROuuqo6j560gbzxEyl1sFt}
pwn.college{tx4FCiYzLL3E9DV9MUJV5Ye6qC3AjyYbC6jDDn0k7DdTkvA}
pwn.college{YtjepMxF25Jftxp1SLMGbLiXSR2a2ebc8i-nCLB4VzM1907}
pwn.college{Ll6gDnzgVBZKXlSzGjz0jZmD088W4RAKVmiVrSpIFkLxLgn}
pwn.college{BQpTdutcDM1WxAUxFQbGHMc0eWo...rkEnIEkNeueWXZXdJ}
pwn.college{2KUK57no44G67Aq.dqll9srshrewCTzX1VSAhdVBFvMbuD3}
pwn.college{9ib8qBn55QkSeL6d72i5cEsW03LmCe2j-BgKII9RkSPERAa}
pwn.college{0WBGcJ4wJ0.FsRU2wBTNAiUssWpWJF60rM-msk3khzStxXr}
pwn.college{4IDz.S6D3pvcShBcuzzDQBoYPB5tmdlM6HXmWWEbT5yT2IS}
pwn.college{AD9msU4CZRUKZv5IxihX66JGnbN2hP9QW5GnRiXiccS5hfJ}
pwn.college{9E5dS3ckTjW4vOsvIGB4P.QxNSTBqn.EEEGv.WNJrM7uLAI}
pwn.college{Lef.lHR6XcbWMymYtQ-YHBjCIIjQ2jMZRHY8A21UWCuyxd5}
pwn.college{.uPTj3k75k3zA3cFcKUUUo2Ze1H5AkluxCSe5TVaTZgpg71}
pwn.college{ADnixDHJKicdmnpYdrYYJ.hYD6OqYGxUuVcJcERQFlomjfG}
pwn.college{7XzS.Y9f8bq7ghOzif4GHcNS0yjFNEKFWmR.zX2whqxthaX}
pwn.college{keKsEucpxKgSa-MpYws8nN1nLkzWBYkiwkcxFqIjoZB-xUx}
pwn.college{NjUWVtwnlVQh6NtypEoJlgirJ8R4pVlHuu4P8CAktT9xMZt}
pwn.college{Dr8rCm5dOttMqtxpcgNKTp3Vg5CNLOYtaYDZuvi0IFXSYVv}
pwn.college{kZ872wm54qq49ZXDUtZfemgJN0HW.1zp0CmKgoXQj4204hJ}
pwn.college{IxwFia9clcZznPNOCSdSJKqW-1tuyfjDm35TRJEQZDAwSBW}
pwn.college{sjC--NgpHx3Bbm5HpZyP-X1MaujTq8pXHMHRsb77ct3Iibd}
pwn.college{TkbK7CTLsUiMWyDHhLQ79AItiD63u2KssvcVl4okstkyODk}
pwn.college{zPrbXD5cXpV7nbKHtWMbVnfHWCeB1DBg7qA9UHXOuDaDLyq}
pwn.college{m-D9nKbkbZLFKQDtUck.ZIu4UUVIJ.OMhxHdaIq8fr.iCx4}
pwn.college{OD.E-0cE8sZVnNXuceXXUew2Z.qny945svr0ulkFw.vUOHK}
pwn.college{yEz9STiGJhfx0xZPLHC86seBviHV5c0lblSvm68PwW7uKKj}
^C
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{Q939hwk1rVgTel-xAQxIDflJOTL.0FNzMDOxwCN0AzNzEzW}

```




