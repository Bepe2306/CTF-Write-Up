# **How to Decrypt?**

in this challenge, i was given a zip file which consist of python file and txt file

**encrypt .py**

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/a88871fd-76f4-4d51-af78-c9650541c90d)


**flag.txt**

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/02b35add-1965-46bb-b83d-f05a6dde226f)

when i analyze the encrypt.py file, i noticed that the algorithm will `modulo 26(%26)` the char, 
since there are 26 alphabeths, i knew that this is a shift cipher.

With the help of my teammate, we were able to recognized that it gets shift 4 times to the right because there is a `+4`

So then i used [dcode Caesar Cipher website](https://www.dcode.fr/caesar-cipher), i took the flag from flag.txt which gave me the flag of this challenge

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/dd8fae83-c5d6-464e-8694-d559c0b0b645)

**FLAG:** `FindITCTF{wh4t_d03s_C43s4r_Do_57hjgnvd8t5}`
