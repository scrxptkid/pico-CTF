# DISKO 2

## Overview:
* Forensics
* Medium

## Description:
Can you find the flag in this disk image? The right one is Linux! One wrong step and its all gone! Download the disk image [here](https://artifacts.picoctf.net/c/539/disko-2.dd.gz).

## Write-up:
Start with downloading and extracting the file:
```bash
$ gunzip disko-2.dd.gz
```
I tried doing
```bash
$ strings disko-2.dd | grep "picoCTF" 
```
But there was a lot of unique flags, so I was going the wrong way.

I was thinking about collecting all the flags and bruteforcing it:
```bash
$ strings disko-2.dd | grep -oP "picoCTF[^}]*}" > out.txt
```
This command would search for a string that start with "picoCTF" and end with "}" so I can get only the flags and not the garbage data.

But this method is too overwhelming.

I hit the hint button and only then realized.

We need to use
```bash
$ fdisk -l disko-2.dd
```
Output
```
Disk disko-2.dd: 100 MiB, 104857600 bytes, 204800 sectors
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disklabel type: dos
Disk identifier: 0x8ef8eaee

Device      Boot Start    End Sectors Size Id Type
disko-2.dd1       2048  53247   51200  25M 83 Linux
disko-2.dd2      53248 118783   65536  32M  b W95 FAT32

```
So, they said in description that the right one is Linux. 

To get familiar with the next command, use:
```bash
$ man dd
```
Extract this image using dd command:
```bash
$ dd if=disko-2.dd of=disko-2.dd1 bs=512 skip=2048 count=51200
```
After, use strings and grep:
```
$ strings disko-2.dd1 | grep "picoCTF"
```
And get the flag!

## Flag
```
picoCTF{4_P4Rt_1t_i5_90a3f3d1}
```
