# **Plane**

in this challenge i was given a picture like the one below

![image](https://github.com/user-attachments/assets/d1d23aee-4048-4186-85c6-4cf95d316cbe)

i was told to find the `latitude` and the `longitude` of the picture.
I use chatgpt to ask what type of tool i can use the find those 2 points, it turns out that `exiftool` can be used to find those points

so when i run exiftool it gave me the `latitude` and the `longitude` of the picture

![image](https://github.com/user-attachments/assets/b1335332-0d71-44be-b4e2-64ead60028ef)

`GPS Latitude                    : 13 deg 22' 12.00" N`

`GPS Longitude                   : 13 deg 22' 12.00" W`

since i dont really understand how to read the lattitude and longitude, i ask chat gpt to explain it a bit and how to find the lattitude and longitude

it turns out that:

- 13 is the `Degrees`
- 22 is the `Minutes`
- 12 is the `Seconds`

and in order to find the real latitude and longitude, there is a formula which was given by chatgpt like the one below

![image](https://github.com/user-attachments/assets/7a150c83-bcf4-4809-8a1a-ca0e08564377)

and then chatgpt also finish the calculation for me from the given degress, minutes and seconds with the formula which will look like the one below which also
brought me to the flag of the challenge

![image](https://github.com/user-attachments/assets/088ed6df-ef18-433e-983e-bf2b6250eac0)

**FLAG:** `n00bz{13.37,-13.37}`
