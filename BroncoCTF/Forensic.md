# **Wario Party**

Who is the true hero of the Mario Party games you might ask? Look inward and you might find it at the intersection of Mario's color and the number of brothers.

Note: This flag is wrapped in broncosec{}

**Solution:**

I was not able to solve this challenge during the CTF, but after i read warlocksmurf Write Up, i found an interesting tool that can be used to solve this challenge

In this challenge i was given a picture of some mario bros characters

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/75d30e52-36d0-496b-95be-7a49d53e9b04)

But the size of this file is too big, so it seems that there is something inside this picture.
So i was using [stegonline](https://georgeom.net/StegOnline/extract) to see if there is any hidden file inside the picture

I was also given an information about the picture:

`Mario's color = Red`

`Number of brothers = 2`

It seems that this challenge is gonna be about LSB (thanks to warlocksmurf Write Up).
So i uploaded the picture, using `LSB` bit order and `R 2` and turns out there is another file inside this picture

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/05b806d1-1b3a-4fc1-9018-532029a0759b)

So i downloaded it and it gives me this picture

![RealHeroOfMario](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/a3de3721-9090-47e8-ac9e-d66149b3e9ef)

I realized that there is a pattern inside the picture so i used this technique:

`Wario = 0`
`Waluigi = 1`

which eventually gives me this set of binary number

```
01100010 01110010 01101111 01101110 01100011 01101111 01110011 01100101 01100011 01111011 00110000 01110111 01110011 00110011 01110010 01011111 01100111 00110000 01110100 01011111 01110100 01101000 00110100 01110100 01011111 01100100 01110101 01101101 01110000 01111001 01111101
```

I use a binary code translator and i get the flag of the challenge

**FLAG:** `bronco{b0ws3r_g0t_th4t_dumpy}`
