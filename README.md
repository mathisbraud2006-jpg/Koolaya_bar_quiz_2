# Koolaya Bar Quiz 2

A lightweight, single-file HTML quiz/game intended to be run in the browser. This repository contains a self-contained quiz app (index.html) that can be opened locally or served from any static hosting.

## Table of contents

- About
- Features
- Getting started
- Usage
- Customizing the quiz
- Developing & testing locally
- Contributing
- License
- Contact

## About

Koolaya Bar Quiz 2 is an HTML-only quiz application built for quick deployment and easy customization. The entire app is contained in `index.html` (HTML, CSS, and JavaScript), making it simple to run, share, and modify.

## Features

- Single-file (index.html) static quiz — no build tools or server required
- Multiple-choice questions
- Score tracking and progress display
- Responsive layout for mobile and desktop
- Easily editable question set inside the HTML/JS

## Getting started

1. Clone or download the repository:

   git clone https://github.com/mathisbraud2006-jpg/Koolaya_bar_quiz_2.git

2. Open the app in your browser:

   - Double-click `index.html`, or
   - Serve the directory with a static server and navigate to `http://localhost:8000` (see "Developing & testing locally" below).

## Usage

- Start the quiz by opening `index.html`.
- Select an answer for each question and submit.
- At the end you'll see your score and (if implemented) any feedback or results.

## Customizing the quiz

The quiz questions and options are defined in the JavaScript inside `index.html`. To change the content:

- Open `index.html` in a text editor.
- Look for a `questions` (or similarly named) array or block of JS objects that define question text, choices, and the correct answer.
- Edit, add, or remove question objects as needed.

Example (pseudocode snippet inside index.html):

```js
const questions = [
  { question: "Example?", choices: ["A", "B", "C"], answer: 1 },
  // ...
];
```

After editing, save the file and refresh the page in your browser.

## Developing & testing locally

To serve the files over HTTP (recommended for some browser features), use a simple static server. From the repo directory:

- Python 3:

  python -m http.server 8000

- Node (http-server):

  npx http-server -p 8000

Then open `http://localhost:8000` in your browser.

## Contributing

Contributions are welcome. Suggestions:

- Open an issue describing the change or bug.
- Fork the repo and submit a pull request with clear changes and a description.

If you want help writing tests or modularizing the code into separate files, open an issue first so we can discuss the desired approach.

## License

This repository does not include a LICENSE file. If you want to allow others to reuse the code, consider adding an open-source license such as the MIT License. To add it, create a `LICENSE` file in the repository root and paste the license text.

## Contact

Repository: https://github.com/mathisbraud2006-jpg/Koolaya_bar_quiz_2

Author: mathisbraud2006-jpg

---

If you'd like, I can also:
- Add a LICENSE file (MIT/Apache 2.0/GPL) for you,
- Extract inline scripts/styles from index.html into separate files (HTML/CSS/JS),
- Create a small demo GIF or screenshot and add it to the README.
