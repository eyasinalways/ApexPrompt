# 🚀 ApexPrompt - Multi-AI Aggregator (Personal Project / Experiment)

![ApexPrompt Banner](https://github.com/eyasinalways/ApexPrompt/blob/main/assets/Screenshot%202026-07-15%20182203.png)

**ApexPrompt** is a personal project exploring how a unified interface could query multiple AI models (ChatGPT, Claude, and Gemini) simultaneously, instead of switching between tabs. Built primarily to learn browser extension architecture, DOM automation, and async messaging patterns.

🔗 **Live Demo:** [www.apexpromt.dev](https://www.apexpromt.dev)

> ⚠️ **Disclaimer:** This is an experimental/educational project. It interacts with AI platforms outside their official APIs by automating their web interfaces via a browser extension. This is **not** how these platforms are officially meant to be accessed, and using it may be against the Terms of Service of ChatGPT, Claude, and Gemini. Use at your own risk — this is not intended as a production tool.

## ✨ Key Features

*   **⚡ Parallel Querying:** Send one prompt and get responses from multiple models at once.
*   **⚖️ Judge AI:** An evaluation layer that compares responses and highlights the most complete/well-formatted one.
*   **🔌 Extension Bridge:** A Chrome Extension (Manifest V3) handles background messaging between the web UI and the automation layer.
*   **💾 Local Session Storage:** Chat history is stored locally in your browser (not synced to any server).
*   **🎨 Dark-mode UI:** Built with Tailwind CSS.

## 🛠️ How It Works (Technical Overview)

1.  The web app sends your prompt to the browser extension's background script.
2.  The extension opens hidden tabs/frames for the selected AI platforms and programmatically fills and submits the prompt via DOM manipulation.
3.  Responses are extracted from the DOM and returned to the web UI.
4.  The Judge AI layer compares the outputs.

If you want to try it locally for learning purposes:

### Step 1: Download the Extension
Upon visiting the site for the first time, you will be prompted to download the **ApexPrompt Bridge Extension**. 
1. Click the "Download Extension" button.
2. Extract/Unzip the downloaded `ApexPrompt_Extension.zip` file on your computer.

### Step 2: Load the Extension
1. Open Chrome and go to `chrome://extensions/`
2. Enable **Developer mode**
3. Click **Load unpacked** and select the `extension` folder from the cloned repo

### Step 3: Run the Web App
Follow the setup instructions in `/web` to run the frontend locally.

## 💻 Technologies Used

*   **Frontend:** HTML5, CSS3, Tailwind CSS
*   **JavaScript:** Vanilla JS (ES6+)
*   **Chrome Extension API:** Manifest V3, Content Scripts, Background Service Workers
*   **Hosting:** Vercel

## 🤖 AI-Assisted Development

The core architecture and logic were designed and implemented by me. I used AI tools (Gemini, ChatGPT) as pair-programmers for:
*   Rapid debugging of syntax and DOM manipulation issues
*   Exploring best practices for Manifest V3 configuration
*   Generating boilerplate, freeing me to focus on core engineering and UI/UX

## 🔜 Roadmap

*   [ ] Rebuild core functionality using official APIs (OpenAI API, Anthropic API, Gemini API) for a proper production-safe version
*   [ ] Add rate limiting and error handling
*   [ ] Improve Judge AI evaluation logic

## 👨‍💻 Developer

**Md. Eyasin**
*   Computer Science & Technology Enthusiast
*   Passionate about Web Development, UI/UX, and Hardware Modifications

Feel free to explore the code, report issues, or suggest improvements!
