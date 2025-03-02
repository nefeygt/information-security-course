
# h6 February2025!

## x) Read and summarize:
1. Schneier 2015: Applied Cryptography: Chapter 1: Foundations:
   - Cryptography ensures confidentiality, integrity, authentication, and non-repudiation.
   - Symmetric encryption uses a shared key for encryption/decryption.
   - Asymmetric encryption uses public/private key pairs.
   - Hash functions create fixed-size digests for data integrity.
   - Digital signatures combine hashing and asymmetric crypto to verify authenticity.
   - Key management is critical: keys must be generated, stored, and exchanged securely.
   - Historical ciphers illustrate basic principles but lack modern security.

2. Karvinen 2023: PGP - Send Encrypted and Signed Message - gpg: <br>
  - Install gpg: sudo apt-get install gnupg.
  - Generate keys: gpg --gen-key.
  - Export public key: gpg --export -a "efe" > public.key.
  - Encrypt a message: gpg --encrypt --recipient "Recipient" message.txt.
  - Sign a message: gpg --sign --encrypt --recipient "Recipient" message.txt.
  - Decrypt: gpg --decrypt message.txt.gpg.
  - Verify signatures: gpg --verify document.sig.
  - Some screenshots from the steps:
    - ![image](https://github.com/user-attachments/assets/c1dae8d2-1e8d-45d4-a74f-8b9b5384f581)
    - ![image](https://github.com/user-attachments/assets/4d8820a6-d854-41d7-bfe6-6f5f08cb6a65)
    - ![image](https://github.com/user-attachments/assets/b94cb9b5-90c8-4ba1-9a8a-57bf44f68794)
    - ![image](https://github.com/user-attachments/assets/1d724cde-b2a4-49a7-9ba5-70dc36375cb0)
    - ![image](https://github.com/user-attachments/assets/96452304-579c-4f4c-ad57-96c905d69b7e)
    - ![image](https://github.com/user-attachments/assets/61986621-798d-4809-9a4d-aee9d4b8cf96)

## a) Install OpenSSH server, connect to it using 'ssh' client.: <br>

![image](https://github.com/user-attachments/assets/dd00547e-3ed7-46b0-925c-59f881fd7312)

## b) Automate SSH connection using public keys: <br>

![image](https://github.com/user-attachments/assets/cbc13964-4d3e-41c0-9c3c-493eafd2f416)

## c) Pretty Good indeed.: <br>

![image](https://github.com/user-attachments/assets/03442db2-70c6-49ac-92bc-329cbff68706)
![image](https://github.com/user-attachments/assets/6b886fda-e5cb-427f-94b5-20ae4f5b9f8a)
I checked a lot but couldn't fix this error:
![image](https://github.com/user-attachments/assets/fed95860-edce-4f64-8465-98beff6b519b)

## d) Password manager: <br>

![image](https://github.com/user-attachments/assets/8a5df53e-8018-440f-9026-ac15ca685641)
![image](https://github.com/user-attachments/assets/07483e73-7ade-4937-85f7-f17aec80bdb3)
![image](https://github.com/user-attachments/assets/292f0c8e-e7e0-4f57-a1a2-9a599cc5f9db)
![image](https://github.com/user-attachments/assets/32aeb795-def1-4888-8ff5-0cb853be5b25)
Why Use?:
A password manager helps protect against:
  - Credential Stuffing → Avoids using the same password on multiple sites.
  - Brute Force Attacks → Generates strong, unique passwords.
  - Phishing Attacks → Autofill only works on legitimate websites.

## m) Voluntary bonus: Encrypt and decrypt messages using a tool other than 'gnupg':
Why age?:
  -Simpler than GPG
  - Modern cryptography
  - No key management complexity
  - Open-source and widely used
Steps:
  1. sudo apt install age
  2. age-keygen -o mykey.txt
  3. grep "^#" mykey.txt | cut -d " " -f 2 (mine is age15re27j6agfwg559m4uyn5mg6jv7xm4q86nkx5vkad87phc45092qm3y90v)
  4. age -r PUBLIC_KEY -o message.txt.age message.txt (encrypt)
  5. age -d -i mykey.txt -o decrypted.txt message.txt.age (decrypt)
![image](https://github.com/user-attachments/assets/d9970353-c062-4bbd-8046-9727abb4ee90)
But it has also some downsides like:
  - Lacks signing (no authentication like PGP)
  - Not as widely adopted as GPG

## n) Voluntary bonus: send and receive encrypted message over email.: <br>

1. I created the key. ![image](https://github.com/user-attachments/assets/459ff000-83ea-48db-975e-5ce15ebcacd2)
2. It's being shown on the key list: ![image](https://github.com/user-attachments/assets/b087563f-58dd-438f-b900-44474b5fbd8a)
3. It all became a huge mess but in the end I managed to create the mail file and encrypt/decrypt it with two users: ![image](https://github.com/user-attachments/assets/9a57b522-e553-445b-ab83-84d08e65ec17)

## o) Voluntary bonus: Find out frequency distribution of letters for a language that you know (other than English). What are the six most common letters?: <br>

I speak Turkish and with a quick google search I found that the most common six letters are: a,e,k,i,l,m

## r) Voluntary bonus: TLS. Choose a transport layer security (TLS) certificate used for the web. Explain key fields. How do you / browser know it's legit? Who says so?
1. Key Fields in a TLS Certificate:
  - Subject
  - Issuer
  - Public key
  - Serial number
  - Validity period
  - Signature algorithm
  - Extensions
2. How Browsers Verify TLS Certificates
  - Certificate Chain Validation: The browser checks the certificate chain to ensure that each certificate in the chain is valid and signed by a trusted CA.
  - Domain Name Matching: It verifies that the domain name in the certificate matches the domain name of the website being accessed.
  - Certificate Revocation Check: The browser checks if the certificate has been revoked by the CA, often using the Online Certificate Status Protocol (OCSP).
  - Signature Verification: It ensures that the certificate's signature is valid and that the certificate has not been tampered with.
3. Who Verifies the Certificate's Legitimacy:
The legitimacy of a TLS certificate is verified by the browser using a list of trusted root Certificate Authorities (CAs) that are pre-installed in the browser or operating system. These CAs are responsible for issuing and managing certificates, and their trustworthiness is established through rigorous security practices and audits.

## s) Voluntary bonus: ETAOIN. Crack this ciphertext:
The last part is probably Tero's website so when we use that and map the letters we get:



## t) Voluntary bonus, easy: try rot13, the military grade top-secret encryption of the top-2 empire of year zero. Could double rot13 provide extra security? Why?:
Why Double Rot13 Doesn't Add Security?
  - Idempotency: Rot13 is its own inverse. That means applying rot13 twice returns you to the original text. For example, if you apply rot13 to a message, and then apply it again, you get the original message back. Therefore, “double rot13” is effectively the same as doing nothing.
  - Lack of Cryptographic Strength: Rot13 is trivial to reverse even once, so doubling it doesn’t add any extra complexity for an attacker. It doesn’t provide any additional cryptographic strength or resistance against attacks.
  - Obfuscation vs. Encryption: Rot13 is often used to hide spoilers or punchlines, not to secure sensitive information. Its simplicity means it’s not secure for protecting data, regardless of whether you apply it once or twice.

### References:
Karvinen 2024: Information Security Course, https://terokarvinen.com/information-security/ <br>
€ Schneier 2015: Applied Cryptography: Chapter 1: Foundations, https://www.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/08_chap01.html#chap01-sec006 <br>
Karvinen 2023: PGP - Send Encrypted and Signed Message - gpg, https://terokarvinen.com/2023/pgp-encrypt-sign-verify/ <br>
Usage Frequency and Training of Letters in Turkish, [https://owasp.org/Top10/A06_2021-Vulnerable_and_Outdated_Components/](https://dergipark.org.tr/tr/download/article-file/441083#:~:text=T%C3%BCrk%C3%A7ede%20en%20s%C4%B1k%20kullan%C4%B1lan%20sesli,%C3%BCst%C3%BCn%2C%20Frans%C4%B1zcaya%20yak%C4%B1n%20oldu%C4%9Funu%20g%C3%B6stermektedir.) <br>
Certificate Validation: How Does a Browser Trust a Certificate?, https://venafi.com/blog/how-does-browser-trust-certificate/ <br>
The Illustrated TLS 1.2 Connection, https://tls12.xargs.org/ <br>
Browsers and Certificate Validation, https://www.ssl.com/article/browsers-and-certificate-validation/ <br>
Wikipedia - ROT13, https://en.wikipedia.org/wiki/ROT13 <br>
Security StackExchange discussions on rot13, https://security.stackexchange.com/search?q=rot13 <br>
