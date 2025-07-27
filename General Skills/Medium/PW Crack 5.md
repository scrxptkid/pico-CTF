# PW Crack 5

## Overview:
* General Skills
* Medium
* Password Cracking

## Description:
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/31/level5.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/31/level5.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/31/level5.hash.bin) in the same directory too. Here's a [dictionary](https://artifacts.picoctf.net/c/31/dictionary.txt) with all possible passwords based on the password conventions we've seen so far.

## Walkthrough
Now this one is tricky. I even had to check the hints to see what's wrong. I consider this as a solid medium level for those who's new to python and programming at all.

This one as PW Crack 4 requires some python skills.

First you open and read a file using with operator. Then, use for loop and use enumerate and print to track the progress. The trick is that document has a whitespaces and you have to use strip() function.

Here's the code:
```python
def level_5_pw_check():
    with open('dictionary.txt', 'r') as d:
        for i, n in enumerate(d):
            if i % 1000 == 0:
                print(f"processed {i} lines")
            n_strip = n.strip()
            
            user_pw_hash = hash_pw(n_strip)
    
            if( user_pw_hash == correct_pw_hash ):
                print("That password is correct", n_strip)
                print("Welcome back... your flag, user:")
                decryption = str_xor(flag_enc.decode(), n_strip)
                print(decryption)
                return
```
And the password is 9581

## Flag 
```
picoCTF{h45h_sl1ng1ng_36e992a6}
```
