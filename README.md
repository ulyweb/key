# System Vault 🔒

A highly interactive, client-side password generator and entropy analyzer built for modern web browsers.

## 🎯 Main Goal
The primary goal of System Vault is to provide a mathematically secure, cryptographically strong key generator that users can run entirely within their browser. It bridges the gap between human-memorable base passwords and high-entropy cryptographic keys, ensuring that your final passwords are mathematically resistant to modern brute-force attacks.

## 💡 Use Case
Whether you are securing a cryptocurrency wallet, a master password manager, or sensitive encrypted volumes, human-generated passwords are the weakest link. System Vault takes a user-defined base string and mixes it with a 256-bit cryptographically secure pseudo-random number generator (CSPRNG) using the `PBKDF2` algorithm. 

By running entirely locally on GitHub Pages, it acts as a transparent, verifiable vault that prevents weak passwords from being compromised.

## ✨ Features
* **Real-Time Entropy Meter:** Analyzes your base password as you type, calculating the exact bit-entropy.
* **Cryptographic Derivation:** Uses the native Web Crypto API (`window.crypto.subtle`) ensuring no data ever leaves your device.
* **Combination Modes:**
  * *Generated Key Only*
  * *Base + Generated Key*
  * *Generated Key + Base*
  * *Random Mix (Fisher-Yates Shuffle)*
* **Brute Force Estimator:** Calculates the time required to crack the key using a cluster of 12x RTX 5090 GPUs against bcrypt (cost 10).
* **Privacy First:** Built-in visibility toggles and a master reset switch prevent shoulder-surfing.
* **Online & Static:** Designed for fast delivery via CDNs. Zero server-side code.

## 🚀 Getting Started
Since this is a client-side only application:
1. Clone this repository.
2. Open `index.html` in any modern web browser or deploy directly to GitHub Pages.

## 🛠️ Built With
* HTML5 / CSS3 / Vanilla JavaScript
* Web Crypto API (`PBKDF2`, `SHA-256`)
* [Anime.js](https://animejs.com/) for fluid, hardware-accelerated dashboard animations.
