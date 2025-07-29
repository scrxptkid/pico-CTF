# Time Machine

## Overview:
* General Skills
* Easy
* git

## Description:
What was I last working on? I remember writing a note to help me remember... You can download the challenge files here:
* [challenge.zip](https://artifacts.picoctf.net/c_titan/160/challenge.zip)

## Write-up
Download the file, unzip it using:
```
bash
$ unzip challenge.zip
```
Next go to the unziped directory:
```bash
$ cd drop-in
```
Check the files in that directory:
```bash
$ ls
```
Read the file using cat command:
```bash
$ cat message.txt
```
The message:
```
This is what I was working on, but I'd need to look at my commit history to know why...
```
Commit history, something related to git. Try using git log to check the logs:
```bash
$ git init
$ git log
```
Logs:
```
commit 89d296ef533525a1378529be66b22d6a2c01e530 (HEAD, master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:22 2024 +0000
```
Then commit using git the hash you got.
```bash
$ git commit 89d296ef533525a1378529be66b22d6a2c01e530
```
And get the flag!

## Flag
```
picoCTF{t1m3m@ch1n3_186cd7d7}
```
