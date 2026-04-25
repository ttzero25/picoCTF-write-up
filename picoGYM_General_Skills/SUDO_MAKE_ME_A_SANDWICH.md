# Fantasy CTF


## Challenge information
```
Level: Easy
Tags: General Skills

Description:
Can you read the flag? I think you can!
ssh -p 54366 ctf-player@green-hill.picoctf.net using password d1a1ff7a
```

Challenge link: https://play.picoctf.org/practice/challenge/735?difficulty=1&page=1

---

## Solution

1. Enter a password after accessing the address given in the problem
<img width="940" height="146" alt="Image" src="https://github.com/user-attachments/assets/fa4b7352-a27d-4eaf-b19c-53c1b28efb77" />
<br>

2. Check existing file -> 'flag.txt' is right there so I tried to check inside with 'cat' but it didn't open due to rights issue
<img width="582" height="66" alt="Image" src="https://github.com/user-attachments/assets/4932b5d7-b2c9-40fc-9405-8af7fbeea91b" />
<br>

3. Use the 'sudo -l' command to verify given permissions
- This confirms that the user can run Emacs with root permissions without a password
- You can get a flag through 'emacs'
<img width="858" height="92" alt="Image" src="https://github.com/user-attachments/assets/0cb6aa6a-467d-4a72-a205-4be998ac9cd2" />
<br>

4. Obtain flag by using the following command
```
sudo emacs flag.txt
```
<img width="683" height="101" alt="Image" src="https://github.com/user-attachments/assets/3fa52167-0c03-48d1-8aa3-c66932033d38" />
<br>

Flag: `picoCTF{ju57_5ud0_17_0cdfe631}`