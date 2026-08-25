# AI Context Assistant Chrome Extension

[![Manifest Version](https://img.shields.io/badge/manifest-v3-blue.svg)](https://developer.chrome.com/docs/extensions/mv3/intro/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

A fast, premium, and feature-rich browser extension to explain, rewrite, translate, and transform selected text on any webpage. Enhance your reading and writing productivity using your preferred LLM provider.

---

## 🌟 Key Features

*   **⚡ Instant Popup & Shortcut Activation**: Highlight any text on any page and press `Alt+O` or right-click to invoke the assistant interface instantly.
*   **🤖 Multi-Provider LLM Support**:
    *   **Google Gemini**: Support for `Gemini 3.5/3.6 Flash` and `Gemini 3.1 Pro`.
    *   **OpenAI**: Support for `GPT-4o-mini`, `GPT-4.1-mini/nano`, etc.
    *   **Anthropic Claude**: Support for `Claude 3.5 Haiku`, `Claude 3.5 Sonnet`, and `Claude 3.5 Opus` (with thinking modes).
    *   **Ollama**: Connect to local or custom hosted models like `Llama 3.1`, `Mistral`, or `Qwen` with custom API base URLs.
*   **🛠️ Core AI Actions**:
    *   **Summarize**: Summarizes the selection in a clean, structured way.
    *   **Rewrite**: Polish the text for natural clarity.
    *   **Explain Like I'm 5 (ELI5)**: Simplifies complicated paragraphs using relatable examples.
    *   **Translate**: Bidirectional translation (e.g., between Arabic and English) with customizable context filters.
    *   **Professional Polish**: Transforms informal thoughts into executive-ready professional messages.
    *   **Bullets Format**: Structurizes walls of text into clean lists.
    *   **Fix Grammar**: Quick proofreading and typo fixes.
    *   **Tweet Hook**: Drafts a social post with hooks matching the highlighted text.
*   **💾 History & Bookmarking**: Keep track of previous conversions, search and browse history, or pin/favorite important entries.
*   **🎨 Premium UI/UX**: Includes seamless system light/dark theme compatibility, clean animations, and micro-interactions.

---

## 📂 Project Structure

The project distribution builds directly into the `dist/` directory, which is ready to be loaded as a Chrome extension.

```text
├── README.md               # Project documentation
└── dist/
    ├── manifest.json       # Extension configurations, permissions, and service workers
    ├── popup.html          # HTML entry point for the extension action popup
    ├── settings.html       # HTML options page for custom settings, provider keys, & prompts
    ├── history.html        # HTML panel for viewing transformation history
    └── assets/             # Bundled application logic (React, CSS, images)
        ├── background.js   # Main background service worker handling API calls & context menus
        ├── content.iife.js # Content script injected into tabs for selections & UI popups
        ├── settings.js     # Settings controller UI script
        └── models-*.js     # Model list mapping & utility modules
```

---

## 🛠️ Installation Guide

Follow these steps to load the extension in Google Chrome or any Chromium-based browser (Edge, Brave, Opera):

1.  **Download/Clone** the repository to your local computer.
2.  Open Chrome and navigate to **Extensions** by entering `chrome://extensions/` in the URL bar.
3.  Toggle the **Developer mode** switch (located in the top-right corner of the Extensions page).
4.  Click on the **Load unpacked** button in the top-left corner.
5.  Select the **`dist`** folder from this project directory.
6.  The **AI Context Assistant** icon will now appear in your browser's toolbar/extension list!

---

## ⚙️ Configuration & Usage

1.  Click the extension icon or open the **Settings** page (options) from the extension management panel.
2.  Configure your desired LLM Provider:
    *   **API Keys**: Add your OpenAI, Claude, or Gemini credentials (saved securely in local browser storage).
    *   **Ollama**: Set up your local URL (e.g., `http://127.0.0.1:11434`) and choose the active model.
3.  Select your default translation target languages.
4.  Highlight text on any website, press **`Alt+O`**, or right-click and select **Open AI Context Assistant** to start transforming!