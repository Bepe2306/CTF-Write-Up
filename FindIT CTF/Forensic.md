# **bagas dribble**

In this challenge i was given a zip file that contains a picture of 'bagas dribble'

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/5b41bc29-745f-4f9c-9c8c-36698d45b4b1)

because this is a forensic challenge, i use exiftool to check if there is any hidden words

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/64ef8ee3-1456-4394-8d56-1d3c0ec9bbdc)

it seems that nothing was hidden in there, so i tried to use command `strings` which straightly gave me the flag of this challenge

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/a91d2440-5390-41f1-942a-1dc9a3ea0db9)

**FLAG** : `FindITCTF{j4ngG4r_4nD_b4g4s_L0v3_t0_dr1bbl3_4cgV9}`

# **File Kosong**

In this challenge i was given a zip file contains a flag.txt file, when i opened it, it's empty

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/47f83c90-06bd-4ac9-a7cc-25fea2155e21)

Because i have done this kind of challenge before, i tried to do `ctrl + a` and turns out there is something in there

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/bc376ebc-a283-4b27-ab0f-d2c02b217551)

I tried to watch a [tutorial](https://www.youtube.com/watch?v=69TBhdrbLEI&ab_channel=R2in3r)  and thanks to the tutorial, i was able to make a python script to decode this blank page
from blank to binary (0 and 1)

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/cf18971b-6029-418c-b45a-286534830e03)

After that i tried to run it which gave me the binary

```
101110011001011010010001100110111011011010101011101111001010101110111001100001001011010011001111101101001010000010111001110011101001001111001100100100011000011011001011101000001011010011001111110010101100111110010001100110001010000010001100110011101011011111000000101000001001100111001000110011001001100010010111100001101001100011001011110010001100011110000010
```

After that i tried to use cyberchef to decode the binary to text, but i did not give me the flag

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/356afa9a-6425-4d01-97be-1ebb67af59f3)

I suspect that something is wrong with the code so i tried to change the 0 and 1 sequence it like the picture below

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/2b6ff024-ce17-4065-b773-284a94d341e4)

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/113f398f-b4e3-4410-b816-3f6fa6dc0891)

```
010001100110100101101110011001000100100101010100010000110101010001000110011110110100101100110000010010110101111101000110001100010110110000110011011011100111100100110100010111110100101100110000001101010011000001101110011001110101111101110011001100010100100000111111010111110110011000110111001100110110011101101000011110010110011100110100001101110011100001111101
```

and then i tried to run it again on Cyberchef which successfully gave me the flag

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/3bd4484d-aca0-4354-b092-d0ef6eb28ff6)

**FLAG:** `FindITCTF{K0K_F1l3ny4_K050ng_s1H?_f73ghyg478}`
