# 🛡️ Fake Review Detector

[![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla%20ES6+-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)

A client-side interactive web utility that simulates fake review detection using heuristic rule-based pattern matching. Designed to showcase frontend DOM manipulation, form validation, and regex string analysis in pure Vanilla JavaScript, HTML5, and CSS3.

---

## 🎯 Features

- **Interactive Review Input**: Clean text area interface allowing users to paste any product or service customer review.
- **Rule-Based Heuristic Analysis**: Real-time evaluation using multiple pattern heuristics:
  - **Length Verification**: Flags suspiciously short reviews (under 20 characters).
  - **Keyword & Phrase Detection**: Regular expression pattern matcher for common promotional buzzwords (great deal, unbelievable, cheap, 100%).
  - **Punctuation Anomaly Check**: Evaluates excessive emotional punctuation (e.g., more than 3 exclamation marks !).
- **Dynamic Visual Feedback**: Instant DOM updates providing color-coded status badges:
  - 🟢 **Safe / Real**: Indicated when the text passes heuristic criteria.
  - 🔴 **Fake / Suspicious**: Indicated when promotional or short patterns are triggered.
  - ⚠️ **Validation Warning**: Alerts if user attempts to evaluate empty input.
- **Zero Dependencies**: 100% lightweight Vanilla JavaScript with no external libraries or build steps.

---

## 🛠️ Tech Stack

- **HTML5**: Semantic document structure and accessible form controls.
- **CSS3**: Centered card layout, responsive container styling, and state classes (.safe, .fake).
- **JavaScript (ES6+)**: DOM Event Listeners, RegExp pattern matching, and input sanitization (	rim()).

---

## 📂 Project Structure

`	ext
mini-project-/
├── index.html       # Primary application layout and review input interface
├── style.css        # Card layout, typography, and status notification styles
├── script.js        # Event handling and heuristic simulation engine
└── README.md        # Project documentation
`

---

## 🚀 Quick Start / Local Setup

Because this is a pure static client-side project, no build tools or package managers are required.

### 1. Clone the Repository
`ash
git clone https://github.com/Ashwani-mic/mini-project-.git
cd mini-project-
`

### 2. Run Locally
Simply open index.html in any modern web browser:
- **Option 1**: Double-click index.html directly from your file manager.
- **Option 2 (VS Code)**: Right-click index.html and select **"Open with Live Server"**.
- **Option 3 (Python CLI)**:
  `ash
  python -m http.server 8000
  `
  Then visit http://localhost:8000.

---

## 🧪 Usage Examples & Test Cases

| Input Review | Triggered Rule | Expected Result |
|---|---|---|
| "Good product!" | Length < 20 characters | 🔴 *This review is likely FAKE.* |
| "Buy this right now, it is an unbelievable and great deal!!!!" | Promotional phrases + Exclamation marks > 3 | 🔴 *This review is likely FAKE.* |
| "The battery life on this laptop easily lasts over 8 hours during normal web browsing and coding." | Normal sentence structure and organic feedback | 🟢 *This review seems REAL.* |

---

## 📌 Future Enhancements
- [ ] Incorporate TF-IDF or sentiment scoring via an NLP API or lightweight WebAssembly model.
- [ ] Add configurable sensitivity thresholds (slider for strictness).
- [ ] Add batch review analysis via CSV upload.

---

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).
