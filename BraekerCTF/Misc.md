# **Eye doctor**

A creaky old bot is zooming in and out of an eye chart. "Can you read the bottom line?" the doctor asks. "No way, " the bot replies. "At a certain distance my view becomes convoluted. Here, I'll make a screenshot."

You and the doctor look at the screenshot. Can you tell what's wrong with the bot's visual processor?

## **Solution:**

In this challenge i was given a picture

![approach](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/09c7de53-f9de-4248-8edc-cd3817d8e413)

From this picture, i can see that there is a flag inside the picture but it is very blurry which means that i have to find another way to clear it.

I tried to google it and i was given 2 options:
1. Increase the contrast
2. Sharpen the image

So i tried to google an online tool to do 2 methods above and i found [pinetools](https://pinetools.com/sharpen-image).
I tried both techniques but turns out it was not enough to make it readable. After analizing the web, i found out that there was a lot of tools that can be used for this image.

So i tried it one by one until i found the `emboss effect`. When i try this tool, it turns out it gave me much readable picture which makes me able to capture the flag

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/0aa7b4e9-1544-4bb5-921c-5185c6f4c7dd)

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/1b51e4c7-571f-4946-b56a-08d2199aa448)

**FLAG:** brck{4ppr04ch1tfr0M4D1ff3r3ntAngl3}
