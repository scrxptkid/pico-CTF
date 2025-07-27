# The Numbers

## Overview:
* Cryptography
* Easy

## Description:
The [numbers](https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png)... what do they mean?

## Walkthrough
Let's take a look at the image.

<img width="387" height="217" alt="the_numbers" src="https://github.com/user-attachments/assets/a2a3c6bc-4d81-46c4-8eb5-1b57197890d5" />

If you have critical thinking you probably noticed that the numbers on the image corresponds to the positions of letters of english alphabet. 

To solve this you can do it manually, which will took too long, or code like I did.

Here's the code:
```python
import string as s


a = s.ascii_uppercase
alp_list = list(a)
print("enter the numbers separeted by space: ")
the_numbers = input()
the_list = the_numbers.split(' ')
stringa = ''
for n in the_list:
    c = int(n)
    b = c - 1
    stringa += alp_list[int(b)]
print(stringa)
```
Run that code and enter the numbers from image separated by space. 

## Flag
After entering the numbers you'll get this
```
PICOCTFTHENUMBERSMASON
```
put the curly brackets where the are needed and.. done!
```
PICOCTF{THENUMBERSMASON}
```
