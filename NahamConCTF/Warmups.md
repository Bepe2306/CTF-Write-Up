# **Uriel**

In this challenge i was given an encoded string in the description

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/3b89a2f6-2185-42ad-83e6-6f40c2754f46)

```
%25%36%36%25%36%63%25%36%31%25%36%37%25%37%62%25%33%38%25%36%35%25%36%36%25%36%35%25%36%32%25%33%36%25%33%36%25%36%31%25%33%37%25%33%31%25%33%39%25%36%32%25%33%37%25%33%35%25%36%31%25%33%34%25%36%32%25%33%37%25%36%33%25%33%36%25%33%33%25%33%34%25%36%34%25%33%38%25%33%38%25%33%35%25%33%37%25%33%38%25%33%38%25%36%34%25%36%36%25%36%33%25%37%64
```

i immediately knew that this is a url encoded string based on my previous ctf experience. So then i use [cyberchef](https://gchq.github.io/CyberChef/) to decode the encoded strings

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/231ba54b-905b-44d8-a378-217e81f8d9ae)

After i decoded it, it gave me another url encoded string, i thought that this is another type of encoded string that very similar to url encoding.

```
%66%6c%61%67%7b%38%65%66%65%62%36%36%61%37%31%39%62%37%35%61%34%62%37%63%36%33%34%64%38%38%35%37%38%38%64%66%63%7d
```

But then i was thinking what if i tried to decode the given url again to see if this is a double url encoded string

After i tried to decode it again, it turns out to be the flag of this challenge

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/1f51ea3e-715d-4d8e-9feb-8ac1431da533)

**FLAG:** `flag{8efeb66a719b75a4b7c634d885788dfc}`


# **Twine**

in this challenge i was given a picture of a twine

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/6bed9c9a-e494-417f-b3bd-0ffbfb2577d0)

and then in the description, i was given a clue that says:

```
Google tells me that twine means: "strong thread or string consisting of two or more strands of hemp, cotton, or nylon twisted together."
```

from the clue above, i knew that the author wass trying to tell us that we can use tool called `strings` to find out the flag, 
so then i execute the command and i add command `grep` so that it will be easier to find it which effectively gave me the flag

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/9e351918-2613-41e4-bed1-c2fdf7ef1e90)

**FLAG:** `flag{4ac54e3ba5f8f09049f3ad62403abb25}`

# **Read The Rules**

i must say that this challenge is quite unique to be done.
So in the challenge description, the author told us this

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/0abe2294-c282-47ac-9636-a9d511010203)

at first, i thought this is gonna be as easy as reading the rules then you will get the flag, but turns out it is not

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/d29acdd6-f893-431c-9d45-84e212e390e0)

After i read the rules above, there was no flag to be seen around the webpage. I thought i had to go to NahamCon CTF's rules server, but it was just the same dead end.

I was thinking where did the author hide the flag, i thought i was not just being sharp enough to find the flag but then i had an idea.

Since the rule of this CTF is written on a web page, what if the flag was hidden in the page source (just like normal website exploitation challenge).
So then i searched the page source of the website and then do a `ctrl+f` to find the flag which successfully gave me the flag of the challenge

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/ba36d2a1-eca5-4f0a-9499-3cade9513012)

**FLAG:** `flag{90bc54705794a62015369fd8e86e557b}`


# **Technical Support**

This challenge is just as simple as open the `ctf-open-ticket` server and get the flag

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/4d93943b-7204-4093-98f3-389ef8dbf160)

**FLAG:** `flag{a98373a74abb8c5ebb8f5192e034a91c}`


# **EICAR**

In this challenge, i was given some random words in a EICAR file

```
X5O!P%@AP[4\PZX54(P^)7CC)7}$EICAR-STANDARD-ANTIVIRUS-TEST-FILE!$H+H*
```

this challenge also gave us a clue that says `What is the MD5 hash of this file?`

So it is just as simple hash the random words to a MD5 hash and wrap it in a flag format

![image](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/2b275d0d-dbcb-4a86-bbba-44c28060fbaa)

**FLAG:** `flag{44d88612fea8a8f36de82e1278abb02f}`
