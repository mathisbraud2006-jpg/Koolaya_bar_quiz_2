# Koolaya Bar Quiz 2

A lightweight, single-file HTML quiz/game intended to be run in the browser. This repository contains a self-contained quiz app (index.html) that can be opened locally or served from any static hosting.

---

## What's changed in this update

I split the original single-file app into separate assets and added deployment tooling and a license:

- Extracted CSS to `styles.css`
- Extracted JavaScript to `script.js`
- Kept `index.html` as the app shell that loads the external CSS/JS
- Added a simple demo SVG at `assets/demo.svg`
- Added an MIT `LICENSE`
- Added a GitHub Actions workflow to publish to GitHub Pages (`.github/workflows/pages.yml`)

All files were committed to the repository in one go. The app still works locally by opening `index.html` or serving the directory using a static server.

---

## Table of contents

- About
- Features
- Getting started
- Run locally
- GitHub Pages (automatic deploy)
- Customizing the quiz
- Contributing
- License
- Contact

## About

Koolaya Bar Quiz 2 is an HTML quiz application built for quick deployment and easy customization. The core app (questions, UI, and logic) was originally embedded in a single `index.html`. For maintainability this update extracts styles and scripts into `styles.css` and `script.js` while keeping the app static (no build step required).

## Features

- Static, client-side quiz app
- Multiple-choice and true/false questions
- Score tracking and simple manual score adjustments
- Responsive design for mobile and desktop
- Easy to customize question sets (JS arrays)

## Getting started

1. Clone or download the repository:

   git clone https://github.com/mathisbraud2006-jpg/Koolaya_bar_quiz_2.git
   cd Koolaya_bar_quiz_2

2. Open the app locally:

   - Double-click `index.html`, or
   - Serve the folder using a static server (recommended):

     python -m http.server 8000
     # then open http://localhost:8000 in your browser

3. The app will load the CSS and JS from `styles.css` and `script.js`.

## Run locally (dev tips)

- For quick iterations, use a simple static server such as Python's `http.server` or `npx http-server -p 8000`.
- When editing the code, refresh the page in your browser.
- Questions are stored in `index.html` (the `Q` object). To move them into a separate file or fetch them from JSON, see the "Customizing the quiz" section.

## GitHub Pages (automatic deploy)

A GitHub Actions workflow is included at `.github/workflows/pages.yml` that packages the repository and deploys it to GitHub Pages on pushes to the `main` branch.

After the first successful run, enable GitHub Pages in the repository settings (Pages -> Source: GitHub Actions). The site will be available at `https://<your-username>.github.io/Koolaya_bar_quiz_2/`.

If you prefer manual setup, you can also serve the `index.html` from the `gh-pages` branch or use any static host (Netlify, Vercel, Surge, etc.).

## Customizing the quiz

- Questions are defined inside the JavaScript (`script.js`), in the `Q` object grouped by category.
- To add or edit questions, open `script.js` and update the arrays (category keys like `films`, `geo`, `musique`, ...).
- To change the theme, edit `styles.css` variables in the `:root` selector.

Example (snippet inside `script.js`):

```js
Q.films.push({
  q: "Exemple de question ?",
  a: "Réponse",
  qt: "Example in English?",
  at: "Answer",
  diff: "facile",
  c: ["Réponse","Option 2","Option 3","Option 4"]
});
```

## Demo

![Demo screenshot](assets/demo.svg)

If you prefer a GIF or PNG, replace `assets/demo.svg` with your image and keep the same path.

## Contributing

Contributions are welcome:

- Open an issue describing a bug or suggestion.
- Fork the repo and submit a pull request.
- If you want help extracting question data to a JSON file or adding tests, open an issue first so we can coordinate.

## License

This project is licensed under the MIT License — see `LICENSE` for details.

## Contact

Repository: https://github.com/mathisbraud2006-jpg/Koolaya_bar_quiz_2

Author: mathisbraud2006-jpg
