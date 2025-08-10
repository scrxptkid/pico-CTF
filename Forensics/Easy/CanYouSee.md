# CanYouSee

## Overview:
* Forensics
* Easy

## Description:
How about some hide and seek? Download this file [here](https://artifacts.picoctf.net/c_titan/4/unknown.zip).

## Write-up:
Download archive and extract the jpg.
```bash
$ unzip unknown.zip
```
You'll get the ukn_reality.jpg file. Let's check for metadata.
Use exiftool:
```bash
$ exiftool ukn_reality.jpg
```
That's what you get:
```
ExifTool Version Number         : 13.25
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2024:02:15 17:40:14-05:00
File Access Date/Time           : 2024:02:15 17:40:14-05:00
File Inode Change Date/Time     : 2025:08:09 23:14:32-04:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 11.88
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fZGVjYTA2ZmJ9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4
                                         
```
Notice the Attibution URL. It's base64. Go to [CyberChef](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%252B/%253D',true,false)) and insert the attr. url.

## Flag
```
picoCTF{ME74D47A_HIDD3N_deca06fb}
```
