# PW Crack 3

## Overview:
* General Skills
* Medium
* Password Cracking

## Description:
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too. There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

## Walkthrough 
Although it's a medium level, I'd consider it quite easy.
 
After using nano and scrolling through the script you can notice a list:
```python
pos_pw_list = ["8799", "d3ab", "1ea2", "acaf", "2295", "a9de", "6f3d"]
```
This list contains 7 possible passwords as said in the description. You can enter them manually or code a bruteforcer as I did. It just more fun plus you improve your coding skills.
Here's the code. It shows you inccorect passwords and the correct one and automatically enters the correct one so you'll get the flag.
```python
def level_3_pw_check():
    pos_pw_list = ["8799", "d3ab", "1ea2", "acaf", "2295", "a9de", "6f3d"]
    for n in pos_pw_list:
    
        user_pw_hash = hash_pw(n)
    
        if( user_pw_hash == correct_pw_hash ):
            print(f'The correct password is: {n}')
            print("Welcome back... your flag, user:")
            decryption = str_xor(flag_enc.decode(), n)
            print(decryption)
            return
        print(f"That password is incorrect: {n}")
```
Correct passsword: 2295

## Flag
```
picoCTF{m45h_fl1ng1ng_6f98a49f}
```
