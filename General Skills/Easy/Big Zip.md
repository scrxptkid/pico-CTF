# Big Zip

## Overview:
* General Skills
* Easy
* Terminal

## Description:
Unzip this archive and find the flag.
* [Download zip file](https://artifacts.picoctf.net/c/505/big-zip-files.zip)

## Write-Up:
First unzip archive.
```bash
$ unzip big-zip-files.zip
```
Go the directory:
```bash
$ cd big-zip-files
```
To find our flag with have to use grep function with -r flag and the pattern. In our case pattern will be "picoCTF". -r flag means it's recursive:
```bash
$ grep -r "picoCTF"
```
And.. get the flag!

## Flag
```
picoCTF{gr3p_15_m4g1c_ef8790dc}
```
