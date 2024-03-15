# **Lootstash**

In this challenge, i got an ELF. i tried to execute the file by running `chmod +x` command first before executing the program.
After i ran it, i got this result

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/c38bbd86-18fa-44ba-8bd4-4745a59a814e)

I found nothing interesting, so i tried to analyze the ELF file in ghidra

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/a5152a5d-11c5-448f-b6c1-8e2d04e4ac6b)

I did not find anything interesting from the main function. So i just tried to scroll it down on the left window and it looks like this

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/5117c12f-f738-47de-954e-620debd5e82b)

I got an idea where everytime i run the program, i got random words these stack of words. It means that probably the flag is in here somewhere, i just need to analyze it more.

So then i tried to scroll it down more and i found the flag

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/fbe0a2b0-989a-43f4-a6ce-4123128201c8)

**FLAG:** `HTB{n33dl3_1n_a_l00t_stack}`


# **Packedaway**

In this challenge i got another ELF file, i use the command `chmod +x` so the file can be executed, but after i run it, i only got this

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/3037b0d3-8358-4597-95b1-c3bf93f1d0b7)

I do not understand what i really should do here, so i just analyze it from ghidra to see if there is any clue.

After analyzing from ghidra, i found just a bunch of function that i do not really understand, but the more i analyze it, the more i found something interesting in ghidra

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/6176aa02-2804-4a0f-b076-10c8f460c798)

It seems that the flag is hidden somewhere in this file but i did not have enough knowledge to find a way to extract it.
I tried to watch some tutorial from youtube till found this [tutorial](https://www.youtube.com/watch?v=0jVikfySiII&t=384s).

It seems that this ELF file is packed in a UPX format.
I tried to follow the tutorial by executing command `strings`

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/93b1865a-eb9d-4786-838c-7a650853b495)

i found a piece of the flag and a confirmation that this file is packed in UPX format

So i tried to unpack it by executing command `upx-ucl -d packed`

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/1bab957d-4b5d-4ccd-bf04-117ddb1d8722)

After i successfully unpacked it, i tried to run command `strings` again but this time with `grep HTB` so i can get the flag instantly

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/7a18695d-d21b-44f6-9d62-4331ef8dda91)

**FLAG:** `HTB{unp4ck3d_th3_s3cr3t_0f_th3_p455w0rd}`
