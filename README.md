# System Vault 🔒 | Enterprise Key Generator (v16.0)

An advanced, educational, airgap-ready digital security tool designed to generate mathematically resilient cryptographic strings and secure passphrases. It operates entirely client-side, making it suitable for high-security environments, digital estate planning, and master password generation.

## 🚀 Features

* **Hybrid Entropy Scoring:** Dual-engine evaluation combining strict Shannon Entropy (mathematical pool calculation) with `zxcvbn` heuristics (human pattern recognition) to perfectly match enterprise password managers like KeePassXC.
* **Cryptographic Quality Tiers:** Dynamically assesses strength from *Low* (< 40 bits) to *Excellent* (≥ 128 bits, representing AES-128 parity).
* **Batch Generation:** Generates 10 distinct, highly secure keys simultaneously, allowing the user to select the option with the most favorable characters and entropy.
* **Omni-Mix Integration:** Fuses a custom Base Modifier, a PBKDF2-derived Cryptographic String, a BIP39-style Passphrase, and the key's own entropy score into a single, unbreakable string. 
* **Omni-Mix Shuffle:** Takes the Omni-Mix output and applies a Fisher-Yates shuffle for absolute cryptographic chaos.
* **Secure Airgap Transfer (QR):** Converts any generated key into a high-density QR code for instant, network-free transfer to a mobile device camera or password manager app.
* **Zero-Trust Execution:** Runs 100% locally in the browser sandbox. No data ever leaves your device.
* **Enterprise UI:** Features a glassmorphism dashboard, hardware-accelerated HTML5 canvas particle background, and real-time threat modeling against modern GPU clusters (e.g., RTX 6000 Ada arrays).

## 🛠️ Usage (Airgap Mode)

This tool is designed to run without an internet connection. To deploy it securely on an offline machine:

1.  Save the `index.html` file to a secure USB drive.
2.  **Required Libraries:** While the provided HTML fetches standard libraries via CDN for convenience, you must download the following files locally to the same directory for a true air-gapped deployment:
    * `anime.min.js` (Animation engine)
    * `zxcvbn.js` (Heuristic scoring)
    * `qrcode.min.js` (QR generation)
3.  Update the `<script src="...">` tags in the HTML `<head>` to point to your local files (e.g., `<script src="./zxcvbn.js"></script>`).
4.  Open `index.html` in any modern web browser.

## 🧠 Threat Modeling & Mathematics

System Vault evaluates brute-force resistance using a benchmark of 150,000 hashes per second (approximating a modern RTX 6000 Ada Generation GPU targeting a bcrypt cost factor of 10). 

* **Strings:** Utilizes the native Web Crypto API (`window.crypto.subtle`) and the `PBKDF2` algorithm to derive highly entropic Base64 output from a base string.
* **Passphrases:** Pulls from an embedded subset of the BIP39/EFF wordlist, dynamically filtering out any words with 4 or fewer letters to mathematically guarantee a higher entropy floor per chosen word.

---
*Built for educational and defensive security applications.*
