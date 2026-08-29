# Telugu Contextual Phonetics Engine 

A lightweight, highly specialized browser-based transliteration tool built for extracting native-sounding English phonetics from **Telugu** text. 

Designed to bridge the gap between rigid machine transliteration and natural human pronunciation, this engine goes beyond standard character-swapping APIs (like Google Translate). It acts as a custom linguistic compiler that understands **contextual pronunciation**—formatting text exactly how a native speaker reads and pronounces it.

![Version](https://img.shields.io/badge/version-1.1.1-blue.svg)
![Zero Dependencies](https://img.shields.io/badge/dependencies-zero-success.svg)
![Tech Stack](https://img.shields.io/badge/tech-HTML5%20|%20JS%20|%20Tailwind-indigo.svg)

---

## 🚀 Why This Tool Exists

Standard transliteration engines blindly swap letters based on strict alphabets. This results in robotic, unnatural English text that forces readers to guess the correct pronunciation. 

This engine is built with **Contextual Phonetic Regex Rules** that mimic human intuition. 

### ✨ Key Features

*   **Context-Aware Phonetics:** Automatically detects phonetic shifts based on surrounding letters (e.g., *[Explain a specific rule here, like: softening 'k' to 'g' in the middle of words, or changing 'm' to 'n' before certain consonants]*).
*   **Domain-Specific Glossary:** Includes a hardcoded dictionary that overrides algorithmic rules to lock in preferred spellings (e.g., standardizing specific cultural terms, brand names, or technical vocabulary).
*   **Native Numeral Conversion:** Automatically converts native **Telugu** numbers (e.g., *[Insert native number like ௧]* -> 1) and triggers smart capitalization for the following text.
*   **Zero Dependencies:** Runs entirely client-side in the browser. No servers, no APIs, no API keys, no installation.
*   **Dark Mode UI:** Built with Tailwind CSS, featuring a clean interface, smooth scrollbars, and an automatic dark/light mode toggle.

## 🛠️ How It Works (The Linguistic Magic)

The engine processes text in three distinct layers:

1.  **The Base Map:** Converts standard **Telugu** characters into their direct English counterparts while managing independent vs. dependent vowels.
2.  **The Contextual Overrides:** Runs advanced Regex patterns to fix unnatural clusters. 
    * *Example:* `[Insert bad machine transliteration]` automatically becomes **`[Insert natural human transliteration]`**.
3.  **The Glossary Lock:** Protects specific words from being altered by phonetic rules, ensuring database consistency for mobile apps and content platforms.

## 💻 Usage

Because this tool is built with vanilla JavaScript and HTML, setup is instantaneous.

1. Clone or download this repository.
2. Open the `index.html` file directly in any modern web browser.
3. Paste your **Telugu** text into the left panel.
4. Click **Transliterate All**.
5. Copy the perfectly formatted English output for your database, app, or document.

## ⚙️ Customization

If you want to adapt this tool for your own domain (e.g., medical, legal, regional dialects, or specific literature), you can easily edit the glossary or phonetic rules.

Open the `index.html` file in any text editor and locate the `transliterate()` function. You can add your own custom overrides here:

```javascript
// Add your own custom dictionary overrides here
return result
    .replace(/\b[native_word_phonetic]/gi, 'YourPreferredSpelling')
    .replace(/\b[another_word]/gi, 'StandardizedSpelling');
