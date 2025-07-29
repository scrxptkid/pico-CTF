# PW Crack 2

## Overview:
* General Skills
* Easy
* Password cracking

## Description:
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.

## Write-up:
Now things get more interesting. Again use nano to open and read the file.
```bash
$ nano level2.py
```
Scroll till line 19 and notice this
```python
if( user_pw == chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39) ):
```
You see these strange data? 0x34, 0x65, 0x63, 0x39. It's a hexadecimal (base-16) numbers. In python chr() converts an integer into its corresponding charachter.
To solve it, you can write a line:
```python
print("password:", chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39))
```
Run a file, and you'll get the password:
```
4ec9
```
Now just enter the password and get the flag!

## Flag
```
picoCTF{tr45h_51ng1ng_9701e681}
```
