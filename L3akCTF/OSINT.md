# *Geosint-1*

In this challenge, i was supposed to guess the exact location from the given picture (basically like geoguesser)

At the beginning, i was only given this picture

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/b891a032-b023-434c-a4ce-371ab3f62b03)

what caught my eyes was the background of this view

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/1953ef8d-e69d-4ae8-81c1-82dea045c8ea)

i can see that there is a very high skyscraper building called One World Trade Center

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/1ff4e033-cfb3-45ce-8794-dc3152480663)

i instantly knew that the picture given in this chall is a road heading to New York City.
But the problem is that i could not find any point of interest that could helped me identified this road.

At first i thought this building can be a point of interest

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/2e845579-c68f-4df5-ac75-8617d8e403f9)

but turns out, i could not really find anything from there, so i kept searching until i found something.

I found a bridge at the back of this picture

![geotry1](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/a3140840-6efb-4796-989e-0b2d62753b57)

usually, a bridge can be a point of interest of a place. So then i tried to do some searching using google image which gave me this result

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/1565d6c6-afa8-47ab-b7e0-f59bfc0ea878)

turns out the bridge name was Verrazzano-Narrows Bridge, then i tried to google it on google maps which gave me this location

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/cad6e4aa-5477-4ac0-b6eb-c6886f34e06a)

since i know that in the picture given, it was heading to New York, with One World Trade Center building as another point of interest,
i tried to set the destination from the bridge to the skyscraper to see the routre it will take

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/077d2d18-fdb5-477a-bcd8-8c79a3901a6d)

it seems that things, start to get interesting.
Since the left view of the road from the picture given was some lake or waters

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/2345e910-6a26-4787-912c-e1ce2a16a296)

so i suggest that the picture was taken on the street, left side of the recommended road. I tried to place the pointer over there which eventually gave me the flag of the challenge

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/74a90e1d-3ebb-43a3-aa36-3f790540114d)

**FLAG:** `L3AK{Verr4zz4n0_Br1dge_1s_pR3tty_c00l}`
