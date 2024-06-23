# **True Freedom**

In this challenge, i was given a Chaewon American flag (IN CHAEWON WE TRUST☝🏻️☝🏻️)

![chaewonn](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/34d0a591-2020-4753-a032-72cfff09da6c)

because this challenge is a forensic challenge, i quickly put it in [aperisolve](https://www.aperisolve.com/45e6cbbb61c5d191a0461e500c833be5) to check if there is something interesting in this photo.
At first, there was nothing interesting but when i check binwalk report, there are several files inside this photo.

I fire up my kali linux and extract the photo with the command `binwalk -e chaewonn.png`

when check into the extracted directory, i found a `ch.txt` file which when i `cat` the file, i got a base64 encoded string

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/ca436e98-d7fc-4f51-8516-ccff3c8adc7e)

I take the base64 to cyberchef to decode it which then gave me the flag of this challenge

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/9ff67e92-22cf-42af-842d-07d3c705be42)

**FLAG:** `CSC{ch43w0n_supr3m4cy}`
