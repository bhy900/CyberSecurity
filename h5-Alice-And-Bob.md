#

## X)

Schneier, B. 2015. Applied Cryptography: Protocols, Algorithms and Source Code in C. 20th Anniversary ed. O'Reilly Media, Sebastopol. Read: 23.11.2026. Available: [https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/].

Chapter 1 - Foundations

1.1 Terminology summary
- Cryptography protects messages by converting plaintext into ciphertext and back using encryption and decryption
- Main security goals are confidentiality, authentication (verifying the sender), integrity (detecting changes), and nonrepudiation (preventing denial of sending a message)
- Modern cryptography relies on keys, not secret algorithms. Security should depend on keeping the key secret
- There are two main types of encryption: symmetric (same/shared key) and public-key (different public and private keys)
- Cryptanalysis is the study of breaking encryption and includes attacks such as ciphertext-only, known-plaintext, chosen-plaintext, and chosen-ciphertext attacks
- A secure algorithm should remain secure even if attackers know how the algorithm works
- Security is measured by the cost, time, data, and computing power required to break the encryption
- Only the one-time pad is considered theoretically unbreakable; most systems depend on making attacks computationally impractical


Chapter 2 - Protocol Building Blocks, sections

2.5 Communications Using Public-Key Cryptography summary

- Public-key cryptography uses two keys: a public key for encryption and a private key for decryption. Anyone can encrypt a message, but only the owner of the private key can read it
- It solves the key-sharing problem of symmetric encryption because users do not need to exchange a secret key in advance
- A typical process is: get the recipient's public key, encrypt the message, send it, and let the recipient decrypt it with their private key
- Public-key encryption is much slower than symmetric encryption and can be vulnerable to some attacks if used directly on message data
- In practice, public-key cryptography is mainly used to securely exchange a temporary session key. The actual message is then encrypted using a faster symmetric algorithm
- This combination of public-key and symmetric encryption is called a hybrid cryptosystem and is widely used in real systems
- Merkle's Puzzles was one of the first public-key concepts, allowing secure communication without a pre-shared key, but it required much more work for an eavesdropper to break than for the legitimate users


Karvinen, T. 2023. PGP - Send Encrypted and Signed Message - gpg. Read: 23.11.2026. Available: [https://terokarvinen.com/2023/pgp-encrypt-sign-verify/].

Karvinen 2023 PGP summary:

- PGP (Pretty Good Privacy) uses public-key cryptography to encrypt messages and create digital signatures. Encryption provides confidentiality, and signing proves the sender's identity
- Each user creates a key pair: a public key that can be shared and a private key that must be kept secret
- Before communicating securely, users exchange public keys and verify their fingerprints to confirm the keys belong to the correct person
- After verification, users can mark each other's keys as trusted and use them for secure communication
- To send a message, the sender encrypts it with the recipient's public key and signs it with their own private key
- Only the recipient can decrypt the message using their private key
- The recipient can verify the sender's signature using the sender's public key, confirming the message was not modified and came from the expected sender
- Public keys can be shared over untrusted networks because security depends on keeping private keys secret

## A)

Online Banking (HTTPS)

I used public key cryptography when logging in to my online bank through a web browser. The website used HTTPS/TLS to create a secure connection.

- The bank's server has a public key and a private key. The public key is included in the website's TLS certificate.
- My browser receives the bank's public key and verifies the certificate.
- My browser uses the public key during the connection setup to securely establish a session key.
- The bank uses its private key to complete the secure connection process.
- After that, both sides use the session key to encrypt the actual banking traffic.


## B)

How different parties use keys:

- Bank server: Keeps the private key secret and shares the public key through its TLS certificate.
- Customer's browser: Uses the bank's public key to verify the server and establish a secure connection.
- Both parties: Use the shared session key to encrypt and decrypt the actual data exchanged during the session.

Security evaluation:

- TLS is considered highly secure and is widely used for online banking.
- The system provides confidentiality, authentication, and data integrity.
- Security depends on protecting the bank's private key and validating certificates correctly.
- The biggest risks are stolen credentials, phishing websites, or compromised devices rather than weaknesses in the TLS protocol itself. 


Sources:

Cloudflare 2024. How Does Public Key Encryption Work? Read: 23.11.2026. Available: https://www.cloudflare.com/learning/ssl/how-does-public-key-encryption-work/

GeeksforGeeks 2025. Public Key Encryption. Read: 23.11.2026. Available: https://www.geeksforgeeks.org/computer-networks/public-key-encryption/

GeeksforGeeks 2026. Understanding SSL/TLS and Digital Security. Read: 23.11.2026. Available: https://www.geeksforgeeks.org/ethical-hacking/how-ssl-tls-certificates-and-digital-signatures-secure-your-online-activities/






## C)

I chose KeePass 3 since I have been using it for a long time.

---
1. Download and install KeePass 2 from public website

<img width="1532" height="422" alt="kuva" src="https://github.com/user-attachments/assets/94f7aaf1-2c4e-4f0d-8d0f-769115e2fac1" />

---

2. Create a database to use and encrypt it

<img width="1077" height="782" alt="kuva" src="https://github.com/user-attachments/assets/0e378338-5d21-4eb6-830a-682f685b0c21" />

<img width="652" height="601" alt="kuva" src="https://github.com/user-attachments/assets/245300d9-c1b8-4663-b2a0-5c63e9659168" />

---

3. Add an entry to store authentication info

<img width="1047" height="660" alt="kuva" src="https://github.com/user-attachments/assets/f807d26a-3280-4a5b-9ee1-2196412ffe4b" />

---

4. Now I can copy&paste username and passsword or use an autofill functionality. 

<img width="1056" height="662" alt="kuva" src="https://github.com/user-attachments/assets/e2333b89-5c0e-4203-9a0a-99eb8d262989" />

---

Several common attacks become easier when people do not use password managers:

- Credential stuffing: People often reuse the same password on multiple sites. If one site is breached, attackers can try the same username and password on other services such as email, banking, or social media
- Brute-force and dictionary attacks: Without a password manager, users tend to create short or predictable passwords that are easier to guess
- Password spraying: Attackers try a few common passwords (such as "Password123") against many accounts. Weak, human-created passwords are more likely to be affected
- Phishing attacks: Password managers usually recognize the correct website URL and autofill credentials only on legitimate sites. Users who enter passwords manually may be more likely to submit them to fake websites
- Security questions and predictable patterns: People often create passwords based on names, dates, or simple variations of old passwords, making social engineering attacks easier

Password managers help by generating long, unique passwords for every service and reducing password reuse. This makes credential stuffing, password guessing, and many phishing attacks much less effective.










