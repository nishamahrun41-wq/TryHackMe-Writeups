# Room Writeup: Overheard at Breakfast

## Room Details
- **Platform:** TryHackMe
- **Event:** Hacker Holidays
- **Category:** OSINT
- **Difficulty:** Easy
- **Room Link:** [Overheard at Breakfast](https://tryhackme.com/room/hh-overheardatbreakfast-6f01793c)

---

## 1. Objective & Scenario
- *Scenario:* Two strangers had a conversation at a breakfast spot and accidentally leaked private details online.
- *Goal:* Use Open Source Intelligence (OSINT) to find their target email/profile and decode the hidden flag.

## 2. Key Tools & Techniques Used
- *Google Dorks:* Simple search operators to locate exact strings across social platforms.
- *MD5 Hashing & Base64 Decoding:* Decoding encoded data strings using standard Linux CLI tools.

## 3. Investigation Logic & Solution Steps
1. **Analyze Transcript:** Extracted the target email address leaked in the breakfast conversation: `lambobytelotushotel@gmail.com`.
2. **Generate Target Identifier:** Used Linux `md5sum` to hash the target email address.
3. **Decode Flag:** Decoded the base64 string found during the investigation to reveal the final flag.

## 4. Key Takeaways
- *OPSEC Awareness:* Never leak personal email addresses or handles in public physical spaces or social bios.
- *Decoding Basics:* Standard encoding formats like Base64 and MD5 hashes are commonly used in CTFs to conceal flags.

---

## Section Code Examples

```bash
# 1. Generate MD5 hash from target email
echo -n "lambobytelotushotel@gmail.com" | md5sum

# 2. Decode the Base64 encoded flag string
echo "VEhNe1MzY3JlVF9QcjBmaWwzX0g0c19iMzNuX0lkZW50MWZpM2R9" | base64 -d
# Flag Output
