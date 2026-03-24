# Log Hunt


## Challenge information
```
Level: Easy
Tags: General Skills

Description:
Our server seems to be leaking pieces of a secret flag in its logs. The parts are scattered and sometimes repeated.
Can you reconstruct the original flag?
Download the 'logs' and figure out the full flag from the fragments.
```

Challenge link: https://play.picoctf.org/practice/challenge/527?category=5&page=1

---

## Solution

1. Download and open the file

<img width="1782" height="784" alt="Image" src="https://github.com/user-attachments/assets/d0a88952-fcd0-4fb7-b69f-68bf1388abca" />

2. Use the file's search function to check logs containing the word "flag."

<img width="847" height="162" alt="Image" src="https://github.com/user-attachments/assets/3ec7d57b-1e3a-4d02-986f-0353a9c3ae96" />

<img width="889" height="126" alt="Image" src="https://github.com/user-attachments/assets/624f0f5a-a918-4bb0-8e0a-6df9d0940520" />

<img width="845" height="163" alt="Image" src="https://github.com/user-attachments/assets/602bcdd7-7d76-4bc0-a1f9-237b2ddb6602" />

<img width="853" height="125" alt="Image" src="https://github.com/user-attachments/assets/9ce8a317-dab5-41e4-a371-1d90b1f5bd26" />

3. Found 4 flag fragments and combined them to complete the flag.

Flag: `picoCTF{us3_y0urlinux_sk1lls_cedfa5fb}`