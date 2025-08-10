# repetitions

## Overview:
* General Skills
* Easy
* base64

## Description:
Can you make sense of this file? Download the file [here](https://artifacts.picoctf.net/c/471/enc_flag).

## Write-up:
After downloading file, use strings to print readable strings.
```bash
$ strings enc_flag
```
Output:
```
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFpSV0VKWVZGVmtNRTVHV2tWU2JYUlVDbUpXV25sVWJGcHZWbGRHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
```
It's a base64. Let's go the [CyberChef](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%252B/%253D',true,false)).
After inserting we see:
```
VjFSQ2EyTXlSblJUV0dSVllrWmFWRmx0TlZOalJtUlhZVVU1YVZKVVZuaFdWekZoWVZkR2NrNVVX
bUZTVmtwUVdWUkdibVZXVm5WUgpiSEJzWVRCd2VWVXhXbXBOUlRWSFdqTnNWZ3BYUjFKeVZGZHdW
MlZzVWxaVmJFNW9UVVJDTlZaWE1XRlZRWEJYVFVkME5GWkVSbXRUCmJWWnlUbFpvVldGdGVFVlhi
bTkzVDFWT2JsQlVNRXNLCg==
```
Hmm, looks like the flag was encrypted by base64 multiple times. Just add more From Base64 recipe until we get the flag.

It took 6 times to get the flag.

## Flag
```
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_9b59b35c}
```
