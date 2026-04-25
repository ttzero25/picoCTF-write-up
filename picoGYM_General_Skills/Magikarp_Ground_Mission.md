# Magikarp_Ground_Mission


## Challenge information
```
Level: Easy
Tags: General Skills

Description:
Do you know how to move between directories and read files in the shell? 
Start the container, ssh to it, and then ls once connected to begin.
Login via ssh as ctf-player with the password, 8c606eb1 on the host wily-courier.picoctf.net and port 54695.
```

Challenge link: https://play.picoctf.org/practice/challenge/189?category=5&difficulty=1&page=3

---

## Solution

1. Connect to the host and port number given in the problem and enter a password
<br>
<img width="804" height="215" alt="Image" src="https://github.com/user-attachments/assets/e2f6f092-33c1-49ee-8c6f-bd0d7c431796" />
<br>

2. Checked two txt files when checking internal files with the 'ls' command. 
First, when checking the '1of3.flag.txt' file as 'cat', I got the beginning of the 'flag'
<br>
<img width="409" height="66" alt="Image" src="https://github.com/user-attachments/assets/0667fa37-e70c-4c56-b394-c3b4fa7733c3" />
<br>

3. If you check the file 'instructions-to-2of3.txt' with the same 'ls' command, see the instructions '/'
```
cd /
cat 2of3.flag.txt
```
<br>
<img width="444" height="76" alt="Image" src="https://github.com/user-attachments/assets/1de12907-ffb2-4a2d-be48-b37e2e730678" />
<br>

4. Found something new when I checked with the 'ls' command to find the 3of3 file. This time it says to use '~'
```
- cd ~
- cat 3of3.flag.txt
```
<br>
<img width="750" height="124" alt="Image" src="https://github.com/user-attachments/assets/39cace8c-844f-4ba5-91d0-047ecb5a1ec4" />
<br>
<br>

Flag: 'picoCTF{xxsh_0ut_0f_//4t3r_0b24fc4f}'