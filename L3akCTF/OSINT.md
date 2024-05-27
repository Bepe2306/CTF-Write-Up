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


# *Geosint-2*

in this challenge, the same like the previous one, i was given a picture

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/c7217a78-4f12-436c-80ef-7facbd76ef5c)

i quickly tried to find the point of interest on this picture, when i turn i right i saw a few russian alphabeths which made me think that this is in russia.
So i tried to use google image to find it

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/900fdab5-72b6-4484-af48-6b67e155227b)

At first, i still had a strong feeling that this picture is in russia, but the more i scroll it the more it began to gave me some random places like Kyiv, Ukraine.

From this clue, it made me realized that, it is not only russia that use russian alphabeths, but there are some country that used to be in the Uni Soviet part that use Russian alphabets as well (sorry nerd stuff).

So then since that picture did not give me any clear clue, i tried to find another point of interest untill i found this stall

![geo2 3](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/2cbfdbd2-cd4b-4709-b11e-36c83bda3a55)

From this point of interest, when i tried to google image it, i found a website that gave me details of the location

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/1532f309-6c4a-4481-bd94-9ef41e28a5a6)

from the map given from this website, i could see that this place is in Karaganda City. But Karaganda City is a quite big city which made me think twice again to find the exact location.

When i tried to zoom out, i found another place that could be a point of interest on the map

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/7955508a-864d-47c3-8cb2-3d20233fb4dd)

there is a cinema called `Sary Arka Cinema 3D`. From this cinema, i tried to use google map to find the exact location

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/4e00be50-3548-43df-8dd7-bd719610d9ac)

It seems that it is very similar to the location given on the other map website. So i tried to choose the right pinpoint on the google map inspired by the pinpoint of the other map website
which turns out was the right location and i got the flag of this challenge

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/d672021a-9616-4e36-9459-e8c77c5d64e1)

**FLAG:** `L3AK{@_Cr0SsR04Ds_1N_kaZAKh5t4N}`
