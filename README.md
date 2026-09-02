# Unicode & Encoding Inspector

Break text into codepoints, compare the four normalization forms, and find invisible characters and homoglyphs hiding in a string. Runs entirely in your browser.

**Live:** <https://unicode-inspector.slippylabs.com/>

## What it does

- Break a string into codepoints with names, categories and escape forms.
- Compare all four normalization forms (NFC, NFD, NFKC, NFKD) side by side.
- Scan for invisible characters — zero-width joiners, soft hyphens, bidi controls, odd spaces.
- Flag homoglyphs: Cyrillic and Greek letters posing as ASCII.
- Copy a cleaned version of the string.

## How it works

This is the tool for 'these two strings look identical and my comparison says they are not'. The answer is nearly always one of three things: a combining sequence that needs normalizing, an invisible character that got pasted along with the text, or a homoglyph — and the inspector shows all three at once instead of making you guess.

## Run it locally

A static site. No build step, no package manager, no dependencies:

```
git clone git@github.com:slippylabs/unicode-inspector.slippylabs.com.git
cd unicode-inspector.slippylabs.com
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Layout

| File | Purpose |
| --- | --- |
| `index.html` | The whole tool |
| `unicode-data.js` | Generated codepoint name, category and confusable tables |
| `style.css` | Styling |

---

Part of [Slippy Labs](https://slippylabs.com). Every tool is indexed at
[projects.slippylabs.com](https://projects.slippylabs.com).
