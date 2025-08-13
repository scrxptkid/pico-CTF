# Binary Search

## Overview:
* General Skills
* Easy
* Shell

## Description:
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses. Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools! You can download the challenge files here:
* [challenge.zip](https://artifacts.picoctf.net/c_atlas/6/challenge.zip)
Additional details will be available after launching your challenge instance.

## Write-up:
Launch instance, use ssh to enter the instance.

```
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 
```

To win in this game you should know the binary search and how it works. Binary search work for O(log n). I really recommend book "Grokking Algorithms" by Aditya Y. Bhargava. This book explains binary search and other algorithms pretty well!

How I solved this CTF:
```
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Higher! Try again.
Enter your guess: 750
Higher! Try again.
Enter your guess: 875
Higher! Try again.
Enter your guess: 938
Higher! Try again.
Enter your guess: 969
Lower! Try again.
Enter your guess: 954
Lower! Try again.
Enter your guess: 947
Congratulations! You guessed the correct number: 947
Here's your flag: picoCTF{g00d_gu355_de9570b0}
Connection to atlas.picoctf.net closed.
```
As you can see, I just took half of the N.

## Flag:
```
picoCTF{g00d_gu355_de9570b0}
```
