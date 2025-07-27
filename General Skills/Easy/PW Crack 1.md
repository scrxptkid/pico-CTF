# PW Crack 1

## Overview:
* General Skills
* Easy
* Password cracking

## Description:
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too.

## Walkthrough 
This one is the easiest CTF ever imo. Just use
```bash
$ nano level1.py
```
to read the file, scroll till line 19 and notice this:
```python
if( user_pw == "8713"):
```
the password is 8713. Now run the file
```bash
$ python level1.py
```
Enter the password and get the flag!

## Flag
```
picoCTF{545h_r1ng1ng_1b2fd683}
```
