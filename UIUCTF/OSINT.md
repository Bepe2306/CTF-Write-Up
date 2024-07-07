# **Night**

In this challenge i was given a picture like this

![chal](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/0a676a24-7e09-4d13-91d7-d8f23afb8148)

from the picture above, i must find the street name and the city name in order to get the flag since that is the format of the flag (`uiuctf{street name, city name}`)

So i quickly use google image to find the road from the picture

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/c9558110-a717-4c73-bf40-59eae909544f)

From here, i could not really find an interesting clue since it just shows some city roads at night.

I tried to find a point of interest several times until i found this tall building

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/ce0c0415-ba5b-4cfd-a02c-3945779b58c1)

When i analyze the shape of the building and even the lighting of the building, it turns out to be the same building from the picture which is the `Prudential Tower`.

So then i search it through the google map and trying to find the similar road from the given picture in the ctf.
Since the given picture is a highway picture, i tried to look up the nearest highway around the building until i found something.

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/f04f78fc-25f1-436a-ad6e-9603b2cb55e2)

there is a highway called I-90 which looks super similar to the picture given from the challenge. Since the challenge obligate me to write the street and city name,
i tried to find the nearest street that looks very similar to the photo which i found one called `Arlington Street`

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/1389ff83-0a70-42c9-a1aa-aaefb85c25e3)

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/12cde274-600e-4fb1-9e0d-0a76f6b7dc9f)

I tried to submit the street name (`Arlington Street`) and the city name (`Boston`) which then enable me to solve this challenge

**FLAG:** `uiuctf{Arlington Street, Boston}`
