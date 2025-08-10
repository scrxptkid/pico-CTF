# Blame Game

## Overview:
* General Skills
* Easy
* Git

## Description:
Someone's commits seems to be preventing the program from working. Who is it? You can download the challenge files here:
* [challenge.zip](https://artifacts.picoctf.net/c_titan/157/challenge.zip)

## Write-up:
Download and unzip the file:
```bash
$ unzip challenge.zip
```
go to drop-in directory:
```bash
$ cd drop-in
```
Use git log to check the commits:
```bash
$ git log
```
Scroll to the very end the notice the flag in the authors name:
```
commit 2466febd40004b9ca644ce924181d07e23dcfaeb
Author: picoCTF{@sk_th3_1nt3rn_cfca95b2} <ops@picoctf.com>
Date:   Tue Mar 12 00:07:06 2024 +0000

    optimize file size of prod code
```

## Flag
```
picoCTF{@sk_th3_1nt3rn_cfca95b2}
```
