# **Secret**

in this challenge i was given a pdf file called `Secret.pdf`

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/1f3443bb-0349-4983-8b07-4bbb62daabdd)

This challenge is very simple since i just need to block the blackout flag and print it to notepad to get the flag

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/3f4056ea-1755-4c7e-932c-a169b98addca)

**FLAG:** `SIVBGR{C0nta1n_Th3_Al13ns}`


# **You Have Mail**

in this challenge i was given an eml file which is a type of mail file, so then i just open the file with the windows mail and it looks like this

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/1ca47fc5-a120-44b9-b80b-cb499693cdab)

in the mail i found a zip file and the password that was decypted in a hex code

**Password :** `53 65 63 75 72 65 5f 43 6f 64 65 3a 4f 72 64 65 72 5f 36 36`

When i tried to open the zip file, it gave me a `txt` file which when i tried to open it, the file requesting a password to open it

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/7195747f-2ae0-4536-b23e-71096ecfe2b4)

So then i use [cyberchef](https://gchq.github.io/CyberChef/) to decrypt the hex encoded code

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/7e4bc694-af79-4ca7-9d88-cd6c19ff471a)

At first i thought the code was only `Code_66` but turns out, the code is the whole decrypted hex which is `Secure_Code:Order_66`

After i gave the password, the txt file gave me the flag of this challenge

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/87dbb518-a097-4b95-86e7-b4abecb5dc0b)

**FLAG:** `SIVBGR{th3_ev1d3nc3_1s_h3r3}`
