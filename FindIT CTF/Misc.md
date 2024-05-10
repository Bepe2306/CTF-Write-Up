# **your journey**

in this challenge, i was given a zip file consist of 2 python file

**source.py**

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/a4861926-5742-4e2f-b7f7-e6e80b8e24fa)

**hidden.py**

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/845dc714-6bb6-4a54-a671-e6ac14ff9111)

in the hidden.py file there are lots of things that will be block when we run the command

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/b9c31835-c902-49f1-bfd7-04b4d1d5ba91)

so then i started running the program. I got a few help from my other 2 teammates while doing this challenge

when i tried to `nc` the ip that was given in the description (`nc 103.191.63.187 1337`), i tried to do print(FLAG) which gave me the result below

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/9a546581-11ce-4e24-bb51-b8c2d808d82a)

We thought this is the flag, so we tried to submitted it but it was incorrect

After a few minutes, my friend was able to identify the way to print out the directory by running the command `print(dir())`

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/b9a45db1-b991-4421-a99f-afc2a9aa8f7e)

Out of all directory that was printed out, only `viewfolder` is not block

I tried to print the viewfolder, which gave me and my teammates another clue

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/8833061e-668e-40d6-bfe2-14040da9bc0a)

Turns out it was a function which then my friend helped me again with the way to use the function

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/408745cf-5f61-48a5-b1c6-6ee1e766a5d9)

Since now we know how to use the viewfolder function, we tried to got into some directories which we finally ended up at challenge directory

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/2f01ac25-754a-46e3-b503-ea973b6df562)

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/c76b65ca-4b52-4de2-9f69-3fc0a9d35326)

we tried to dig deeper which eventually brought us to the flag (but we were too late to submit the flag)

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/62e5af1a-7e73-4c32-b57e-02450a992eda)

**FLAG:** `FindITCTF{4m0GU5_y0u_Sh0u1d_ch3ck_4ll_th3_f1l3s}`
