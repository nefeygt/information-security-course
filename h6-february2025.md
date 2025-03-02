
# h6 February2025!

## x) Read or watch and summarize: € Schneier 2015: Applied Cryptography: 2.3 One-Way Functions and 2.4 One-Way Hash Functions.
1. One-Way Functions:
   - A function is one-way if it’s easy to compute in one direction but computationally infeasible to reverse.
   - Example: Multiplying two large primes is easy; factoring the product back into primes is hard.
   - Used in cryptographic systems like RSA for key generation.
2. One-Way Hash Functions:
   - A hash function takes an input (of any size) and produces a fixed-size output (hash).
   - Properties:
      - Preimage resistance: Given a hash, it’s hard to find the original input.
      - Second preimage resistance: Given an input, it’s hard to find another input with the same hash.
      - Collision resistance: It’s hard to find two different inputs with the same hash.
   - Examples: MD5 (broken), SHA-1 (deprecated), SHA-256 (secure).
   - Applications: Digital signatures, password storage, data integrity checks.

## a) Install Hashcat. Test it with a sample hash.: <br>
I followed the steps as shown on Tero's page:
![image](https://github.com/user-attachments/assets/406ae22c-f22b-402e-8008-de98f059c193)
I downloaded the Rockyou dictionary:
![image](https://github.com/user-attachments/assets/b3c06815-3695-4cf1-b50d-d5760c13fc14)
And I successfully cracked the hash:
![image](https://github.com/user-attachments/assets/67e23b12-4bee-4237-b9a9-598a5416f88d)

## b) Crack this hash: d595b2086532422bbe654bc07ea030df: <br>
I changed the command from the before question:
![image](https://github.com/user-attachments/assets/8080772b-baa2-441e-850a-9251b859262e)
Then it successfully cracked the hash using the dictionary:
![image](https://github.com/user-attachments/assets/d7085c13-b31c-43f1-97a4-0d2e6fb1c5c1)

## m) Voluntary: Compile John the Ripper, Jumbo version.: <br>
I followed the steps on Tero's page:
![image](https://github.com/user-attachments/assets/51314f12-1710-4e0c-a194-1d3b125b22cd)
![image](https://github.com/user-attachments/assets/01c2bd10-f8df-435b-af42-3dfe99689698)
![image](https://github.com/user-attachments/assets/104dc32c-5db7-4e81-8a7f-67657394611d)
![image](https://github.com/user-attachments/assets/2d856bb3-ce92-49d2-a39e-3bbad1f08426)
I cracked it:
![image](https://github.com/user-attachments/assets/d81b0b13-b9b3-4ef8-87c3-f65cb7aad30b)

## n) Voluntary: Crack a zip file password: <br>
I created a zip file and by following the steps from the last question I cracked it's password and it's correct!
![image](https://github.com/user-attachments/assets/2146f467-32ae-48f9-b17c-9c8c575620f0)

## o) Voluntary: create a password protected file other than ZIP. Crack the password. How many formats can you handle?:

## p) Voluntary: Watch and summarize: : <br>
- Jackpotting: Attackers physically access ATMs to install malware or hardware devices, forcing the machine to dispense all its cash.
- Techniques:
   - Exploiting outdated software or weak physical security.
   - Using malicious USB devices or network attacks.
- Prevention:
   - Regular software updates.
   - Strong physical security (e.g., tamper-proof seals).
   - Monitoring for unusual activity.
- Impact: Millions of dollars stolen globally, highlighting the need for robust ATM security.

### References:
Karvinen 2024: Information Security Course, https://terokarvinen.com/information-security/ <br>
€ Schneier 2015: Applied Cryptography: 2.3 One-Way Functions and 2.4 One-Way Hash Functions., https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec003 <br>
Karvinen 2022: Cracking Passwords with Hashcat, https://terokarvinen.com/2022/cracking-passwords-with-hashcat/ <br>
Karvinen 2023: Crack File Password With John., https://terokarvinen.com/2023/crack-file-password-with-john/ <br>
Jackpotting ATM's (Automated Teller Machines) - Its easier than you might think - Alexander Forbes, https://www.youtube.com/watch?v=ThPJrPf7O2s <br>

