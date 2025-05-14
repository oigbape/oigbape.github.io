---
title: "Applied Cybersecurity: Vulnerability Analysis & Exploit Demonstrations"
order: 2
collection: portfolio
excerpt: "Hands-on analysis and implementation of common attacks in controled enviroments, covering compilation process, buffer overflows, format string attacks, SetUID, environment variable exploits, secure random number generation, secret/public-key encryption (RSA, PKI), padding oracle attacks, and hash length extension attacks"
#date: YYYY-MM-DD # e.g., 2024-12-15 (or semester)
#tags: [Cybersecurity, Ethical Hacking, Vulnerability Assessment, Cryptography, C, Python, Linux Security, Buffer Overflow, Format String, SetUID, RSA, PKI]
Key Technologies: "C, Python, GDB, Linux Security, and Cryptography (Symmetric/Asymmetric, RSA, PKI, Hashes)"
#github_url: "[Link to relevant GitHub repo if available]"
# report_url: "[Link to lab reports if available]"
# image_path: "/images/portfolio/cybersecurity-lab-teaser.png"
---
## Objective
To gain practical understanding and experience of common software vulnerabilities, memory corruption attacks, secure programming principles, the workings of cryptographic primitives, and common attacks against cryptographic systems.

* **Compilation Lab:**
   * Explored the step-by-step C compilation process (preprocessing, compilation, assembly, linking) using `gcc`.
   * Analyzed executable sections using `objdump` and observed the impact of debugging flags (`-g`).
   * **Skills:** C Compilation, ELF Format, Debugging Information, `gcc`, `objdump`.

* **Buffer Overflow Attack Lab (Set-UID Version):**
   * Developed exploits for a program with a buffer overflow vulnerability to gain root privileges in a Set-UID environment.
   * Crafted shellcode (32-bit & 64-bit concepts) and manipulated stack layouts, including return addresses.
   * Investigated and bypassed (or understood limitations of) countermeasures like Address Space Layout Randomization (ASLR), non-executable stack (NX bit), and StackGuard.
   * Explored attacks of varying difficulty levels based on buffer size and system architecture (32-bit vs. 64-bit).
   * **Skills:** Buffer Overflow Exploitation, Stack Manipulation, Shellcode, ASLR, NX Bit, StackGuard, SetUID Vulnerabilities, GDB, Python (for exploit scripting), C.

* **Format String Attack Lab:**
  * Exploited format string vulnerabilities in a C program to crash the program, read internal memory (stack and heap data), modify program memory (arbitrary write), and inject/execute shellcode to achieve a reverse shell.
  * Constructed format string payloads to manipulate the program's execution flow by overwriting return addresses or other critical data structures.
  * Worked with both 32-bit and 64-bit targets, addressing challenges like null bytes in 64-bit addresses.
  * **Skills:** Format String Vulnerabilities, Memory Corruption, Arbitrary Memory Read/Write, Shellcode Injection, Reverse Shell, Python, C, GDB.

* **Environment Variable and Set-UID Program Lab:**
  * Investigated how environment variables (PATH, LD_PRELOAD, LD_LIBRARY_PATH) affect program behavior, especially in privileged Set-UID programs.
  * Demonstrated how an attacker can manipulate PATH to execute arbitrary commands and exploit LD_PRELOAD to load malicious shared libraries.
  * Explored differences between `system()` and `execve()` for invoking external programs in Set-UID contexts.
  * Analyzed capability leaking in Set-UID programs after privilege revocation.
  * **Skills:** Linux Environment Variables, SetUID Program Security, PATH Hijacking, LD_PRELOAD Attacks, Secure Program Invocation, Capability Leaking, Shell Scripting, C.

* **Pseudo Random Number Generation Lab:**
  * Analyzed vulnerabilities in using time-based seeds for pseudo-random number generators (PRNGs) like `srand(time(NULL))`.
  * Performed an attack to guess an encryption key generated with a weak PRNG by exploiting a known plaintext and a narrow time window.
  * Explored Linux kernel entropy sources (`/proc/sys/kernel/random/entropy_avail`) and the behavior of `/dev/random` (blocking) vs. `/dev/urandom` (non-blocking).
  * Learned to generate cryptographically secure random numbers using `/dev/urandom` in C.
  * **Skills:** Cryptography, PRNG Security, Entropy, Known-Plaintext Attacks, C, Linux System Internals.

* **Secret-Key Encryption Lab:**
  * Performed frequency analysis to break a monoalphabetic substitution cipher.
  * Used `openssl enc` to encrypt/decrypt files with various ciphers (e.g., AES) and modes (ECB, CBC, CFB, OFB).
  * Analyzed the visual impact of ECB vs. CBC mode on image encryption.
  * Investigated PKCS#5/PKCS#7 padding in block ciphers and error propagation in different modes.
  * Exploited vulnerabilities related to IV reuse (known-plaintext attack on OFB) and predictable IVs (chosen-plaintext attack on CBC via an encryption oracle).
  * Developed a C program using OpenSSL's `libcrypto` to brute-force an AES-128-CBC key.
  * **Skills:** Symmetric Cryptography (AES), Encryption Modes (ECB, CBC, CFB, OFB), Padding Schemes, IV Security, Frequency Analysis, Known-Plaintext Attacks, Chosen-Plaintext Attacks, OpenSSL (command line & libcrypto), C.

* **Padding Oracle Attack Lab:**
  * Implemented a padding oracle attack against an AES-CBC encrypted secret message by interacting with an oracle that only revealed whether padding was valid.
  * Iteratively decrypted ciphertext blocks byte-by-byte by manipulating IVs or preceding ciphertext blocks and observing the oracle's response.
  * Automated parts of the attack process using Python.
  * **Skills:** Cryptography (AES-CBC), Padding Oracle Attacks, Chosen-Ciphertext Attacks (CCA), Python, Hex manipulation.

* **Hash Length Extension Attack Lab:**
  * Exploited the vulnerability in naive MAC constructions (e.g., `SHA256(key || message)`) to append data to an original message and forge a valid MAC without knowing the secret key.
  * Constructed the necessary padding and new MAC for the extended message.
  * Demonstrated the attack against a sample web server that used this insecure MAC scheme.
  * Implemented the fix using HMAC-SHA256 to mitigate the vulnerability.
  * **Skills:**: Cryptography (Hash Functions, MACs), Hash Length Extension Attack, HMAC, Python, Web Security Concepts.

* **RSA Public-Key Encryption and Signature Lab:**
  * Implemented core RSA algorithm steps using C and the OpenSSL BIGNUM library: private key derivation (given p, q, e), encryption, decryption, message signing, and signature verification.
  * Worked with large number arithmetic for cryptographic operations.
  * Manually verified an X.509 certificate by extracting the issuer's public key, the server certificate's body, and the signature, then performing RSA signature verification.
  * **Skills:** Asymmetric Cryptography (RSA), Public/Private Key Generation, Encryption/Decryption, Digital Signatures, X.509 Certificates, OpenSSL (BIGNUM library), C, Number Theory basics.

* **Public-Key Infrastructure (PKI) Lab:**
  * Acted as a Certificate Authority (CA) to generate a self-signed root CA certificate using OpenSSL.
  * Generated Certificate Signing Requests (CSRs) for a web server, including Subject Alternative Names (SANs).
  * Signed server CSRs with the created CA to issue X.509 certificates.
  * Deployed the server certificate and private key on an Apache HTTPS website.
  * Analyzed browser trust errors and resolved them by importing the custom root CA certificate into the browser's trust store.
  * Simulated and analyzed Man-in-the-Middle (MITM) attacks against HTTPS, demonstrating how PKI defends against them and the consequences of a compromised CA.
  * **Skills:** PKI, X.509 Certificates, Certificate Authority (CA) operations, OpenSSL (certificate management), Apache HTTPS configuration, SSL/TLS concepts, Man-in-the-Middle Attacks, Digital Trust.

## Key Outcomes & Learnings Across Labs
 * Gained extensive hands-on experience in identifying, exploiting, and mitigating a wide range of common software and cryptographic vulnerabilities.
 * Developed proficiency in using C and Python for security analysis, exploit development, and cryptographic programming.
 * Mastered the use of debugging tools (GDB), hex editors, and command-line utilities (OpenSSL, gcc, objdump) for security tasks.
 * Deepened understanding of Linux system internals, SetUID program behavior, and process environment manipulation.
 * Acquired practical skills in both symmetric and asymmetric cryptography, including encryption modes, padding, hashing, MACs, digital signatures, RSA, and PKI.

## Artifacts
* **Lab Reports:**  
* **Code Snippets/Exploits:**  
