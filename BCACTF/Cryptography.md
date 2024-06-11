# **Vinegar Times 3**

in this challenge, i was given 3 decrypted words and a cipher key that looks like these

```
key - vinegar

cipher 0 - mmqaonv

cipher 1 - seooizmt

cipher 2 - bdoloeinbdjmmyg <- THIS ONE
```

From here i analyze the challenge and i just realized that the challenge said `Vinegar` which rhymes with the word `Vigenere` which is a type of cipher. So i just use
[dcode Viginer Decoder](https://www.dcode.fr/vigenere-cipher)

The first step that i take is to decrypt cipher 0 with the provided key which gave me an answer `redwine`

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/62c5a5b5-d405-4388-b7eb-749c2a62eb85)

by having this word, i suspect that it is another key to another cipher which is cipher 1. So then i just user redwine as a key to decrypt cipher 1.

Again from here i found another answer which is `balsamic`

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/28800eda-9d4f-4280-b8c3-493bae2dd870)

Just like the previous one, i use balsamic as the key to decrypt the cipher 2.
When i decrypt it, i found an answer `addtosaladyummy` which is the flag of this challenge

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/51ee4078-b08c-4fd6-8bfb-3178e3ce3035)

**FLAG:** `bcactf{add_to_salad_yummy}`
