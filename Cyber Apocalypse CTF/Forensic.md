# **It Has Begun**

in this challenge, i was given a script.sh file. When i opened it, this is what is inside the file

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/e7ea046f-7eb8-4c09-bd5f-28ffea2735cd)

i can already see that there is a piece of flag inside of it, i just need to reverse it using cyberchef

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/4b05b733-865d-49b3-87e3-f90e92570e26)

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/c23dd9eb-fb0a-4c91-a4ac-e9e4f644f0bf)

when i saw the rest of encrypted data, i thought it was the rest of the flag but just encrypted in base64 but when i tried to decrypt it, it was not the flag.
I tried to do more analyze in the file then i found something interesting. I found a base64 that gets seperated from other base64 and seems very suspicious

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/98b54c95-7d25-4e6a-91cf-b77c6d78bc3f)

i tried to decrypt it using cyberchef which turns out is the other part of the flag

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/8921411b-e825-44b6-b1c1-cd8a7cc61872)

**FLAG:** HTB{w1ll_y0u_St4nd_y0uR_Gr0uNd!!}
