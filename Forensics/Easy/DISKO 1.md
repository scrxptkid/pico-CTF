# DISKO 1

## Overview:
* Forensics
* Easy
* Image

## Description:
Can you find the flag in this disk image? Download the disk image [here](https://artifacts.picoctf.net/c/538/disko-1.dd.gz). 

## Write-up:
Download the .gz file and extract it:
```bash
$ gunzip <filename.gz>
```
Use strings and grep to find the flag:
```bash
$ strings disko-1.dd | grep "picoCTF"
```
Strings command passes only readable lines through pipe operator (|) to grep which searches for our flag by "picoCTF".

## Flag
```
picoCTF{1t5_ju5t_4_5tr1n9_e3408eef}
```
