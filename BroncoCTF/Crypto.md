# **Preschool Lessons**

a b c... easy as 1 2 3...

Do you REALLY know your ABCs?

```
abbaaabacabbbaabacabbabbbbcabbabbbacabbaaabbcabbabbbbcabbbbabbcabbabaabcababbbbbcabbabbabcaabbaaabcabbbaabbcabbbaabbcababbbbbcabbbaaaacabbbaabacaabbaabbcabbbaabbcabbaaabbcabbabaaacabbabbbbcaabbaaaacabbabbaacabbbbbab
```

**Solution:**

When i got the cipher message, i knew that there is some encryption technique has been done there but i was not able to identify it so the challenge was not able to be solved before the CTF ended.
However, after reading warlocksmurf write up, it turns out that the encrypted message can be turned into binary numbers by using this technique:

1. Replace `a` with `0`
2. Replace `b` with `1`
3. Replace `c` with `space`

I tried to do it in cyberchef which turns out gave me the flag of this challenge

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/4162a710-b002-4984-8655-e3c8de686ec8)

**FLAG:** `bronco{i_m1ss_pr3scho0l}`

# **Zodiac Killer**

The Zodiac Killer is on the loose! I saw this message spray painted on a wall.

Wrap the flag in bronco{}

**Solution:**

In this challenge i was given a picture consist of many symbols

<img width="473" alt="zodiacchal" src="https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/bd337abc-1270-45f4-b824-a4ad6f702408">

When the name of the challenge said "Zodiac Killer", i instantly search zodiac killer decoder and found [dcode zodiac killer cipher](https://www.dcode.fr/zodiac-killer-cipher)

It turns out that i just need to input the symbols into the decoder and i after i decode it, i got the flag

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/5e549e0e-229b-4fe5-add9-814dfc99c8c0)

FLAG: `bronco{LOOKOVERYOURSHOULDER}`

# **Electrical Engineering**

I hate electrical engineering

**Solution:**

In this challenge i was given a PDF file which consist of 4 pictures

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/d0c5ad9b-81e6-408b-a5ad-ce494637c896)
![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/d8f53f11-ab8f-4724-b70f-a46058b4be1a)
![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/9c912704-9428-40bd-ad19-841d594a9645)
![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/d245356f-fc67-4c99-9614-edb0c8c48814)

I was really confused about what to do with these resistors so i was not able to finish this challenge before the CTF ended. But after i read warlocksmurf Write Up again, i found a very interesting tool called [Geocaching](https://www.geocachingtoolbox.com/index.php?lang=en&page=resistorCode).

This tool is able to count the resistance of the resistors based on the band colors of the resistor, Example:

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/0498560b-aded-41bd-a4de-9cde8c912afe)

So i tried to count all resistors in the picture which gives me this set of numbers

`98 114 111 110 99 111 123 114 69 115 105 53 116 95 101 118 49 76 125`

After that i put it in the Cyberchef and use `From Decimal` recipe which gave me the flag of this challenge

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/fa8acc5f-b404-4599-938c-3907e0550a20)

**FLAG:** `bronco{rEsi5t_ev1L}`
