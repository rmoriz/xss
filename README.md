# xss

Tiny static site deployed to GitHub Pages. `script.js` runs `alert()` on window load.

Live: <https://rmoriz.github.io/xss/>

## How it works

- `index.html` loads `script.js` with `defer`.
- `script.js` registers a `load` listener on `window` and calls `alert()` when the page has loaded.
- Pushes to `main` deploy via the `Deploy to GitHub Pages` workflow (`.github/workflows/pages.yml`).

## Local preview

```sh
python3 -m http.server 8000
# open http://localhost:8000/
```
