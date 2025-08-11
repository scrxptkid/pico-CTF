# Glory of the Garden

## Overview:
* Forensics
* Easy

## Description:
This [garden](https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg) contains more than it seems.

## Write-up:
Download garden.jpg. Since it's foresincs, we can try checking metadata, we can check for steganography and check for the hex.

Checking for metadata and steganography give us nothing, so let's check the hex. Use hexeditor command in kali linux:
```bash
$ hexeditor garden.jpg
```
Press 'W' to search for the text string and enter "picoCTF" and get the flag!

## Flag
```
picoCTF{more_than_m33ts_the_3y33dd2eEF5}
```
