# MultiCode


## Challenge information
```
Level: Easy
Tags: General Skills

Description:
We intercepted a suspiciously encoded message, but it’s clearly hiding a flag. 
No encryption, just multiple layers of obfuscation. Can you peel back the layers and reveal the truth?
Download the message.
```

Challenge link: https://play.picoctf.org/practice/challenge/710?page=2

---

## Solution

1. Download a given file and check its contents
<img width="475" height="353" alt="Image" src="https://github.com/user-attachments/assets/4c4c89fa-9a05-4ba9-8603-9d17f183e017" />
<br>

2. The string is encoded in a total of 4 steps
<br>
- Base64
```
[Clue]
Character set only uses A-Z, a-z, 0-9, +, /
= or == padded at the end
Multiple of 4 in length
a meaningless string that cannot be read by a person
```
<br>

- Hex
```
[Clue]
0-9, use a-f characters only (no g-z)
Long without blank space
Even length (2 letters = 1 byte)
Values in the ASCII range (20–7e) such as 63 → c, 76 → v
```
<br>

- URL decode
```
[Clue]
% Hex is repeated in the back 2 digits
%7B = {, %7D =} is a very frequent pattern
The rest of the characters are just read (mixed)
``` 
<br>

- ROT13
```
[Clue]
The structure looks similar to picoCTF{...}
You can push cvpbPGS ← picoCTF 13 compartments
Only the alphabet is replaced, and the numeric/special characters remain the same
c→p, v→i, p→c, b→o regularity seen
```

3. Decode the values obtained for each step in order

1) Base64 Decoding -> 637670625047532537426172666772715f72617030717661745f317137356f723633253744
2) Hex Decoding -> cvpbPGS%7Barfgrq_rap0qvat_1q75or63%7D
3) URL Decoding -> cvpbPGS{arfgrq_rap0qvat_1q75or63}
4) ROT13 Decoding -> picoCTF{nested_enc0ding_1d75be63}



Flag: 'picoCTF{nested_enc0ding_1d75be63}'