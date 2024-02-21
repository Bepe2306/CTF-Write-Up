# **Keyboard Elitist**

My buddy is bragging about how cool his Framework laptop is and how much faster he can type than me. When I tried to type a message, it came out as garbage!

```
A;;apfkgij gj;ukd ar ut ghur war a Qwfpgj efjbyaps yk a Cyifmae uk;lg rchfmf maefr ghur iyye iuef dapbadf. Mj tpufks ur sftukugfij a efjbyaps rkyb, ylg hfpf wugh hur mysliap tpamfwype ia;gy;. Rudh, fughfp waj... hfpf ur ghf tiadO bpykcy{qwfpgj_vr_c0ifm@e}
```

**Solution:**

At first, i thought this is either base64 cipher or subtitution cipher, so i tried using those ciphers to decode it but it seems those ciphers are not the answer.

But then i randomly tried another similar cipher called Mono-Alphabetic Subtitution by using  [dcode](https://www.dcode.fr/monoalphabetic-substitution) that turns out gave me the flag of the challenge

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/cc8effc3-f52c-4b0b-91b0-3e87f0078d79)

**FLAG:** `BRONCO{QWERTY_VS_C0LEM@K}`

# **Shrekanana Banana**

I was given this image of Shrek in a Banana, but I can't help but feel like I am missing something...

**Solution:**

From this challenge, i was given a PNG image like the image below

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/30976f91-5da1-454e-a29d-3ce817f56738)

The only technique i can think of first when it comes to PNG is to use stegsolve to see if there is any hidden message or flag inside the picture

So i use the command `java -jar stegsolve.jar` to launch the stegsolve and then i keep switching the image in stegsolve until i found the flag at `Green plane 2`

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/d2e2e42b-6be8-48c1-876b-e30bd57dcd22)

**FLAG:** `bronco{shr3konogr@phy}`

# **Stego-Snore-Us**

I'm not the only one tired after pulling an all-nighter for Hack for Humanity...

**Solution:**

In this challenge, i got another PNG image again

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/98528749-848d-4293-92bf-6aaa417f1523)

And like the previous challenge, i simply use stegsolve and kept switching the image to analyze if there is a hidden flag inside of it

When i reach **Blue plane 1**, i found an encrypted flag

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/44ae9f2e-c49f-4804-bfe7-470abaff5650)

**Encrypted Flag:** `pesxas{xs_isez_qjj_xkowuzeh}`

Based on the picture above, i knew that there was a cipher being used at this challenge to encrypt the flag, but i was not able to solve this challenge before the CTF ended.

Nevertheless, after the CTF ended, i read warlocksmurf Write Up to get some knowledge about this challenge and i found something interesting.

It turns out that the cipher that was being used in this challenge was Mono-Alphabetic cipher. By using an open source tools called [quipquip](https://quipqiup.com/), i was able to extract the flag

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/aa472d79-fb47-4e7e-9347-7eff8b2177d6)

**FLAG:** `bronco{no_more_all_nighters}`
