# stayhoneywoods.com

The website for Honeywoods, a rental home in Stanfordville, New York.

The working rules and security rules are in a steering file that is kept out of this repository. Ask James for a copy and save it as `private/STEERING.md`. Read it before making a change.

## Preview on your computer

```bash
python3 -m http.server 4173 --bind 127.0.0.1
```

Then open http://127.0.0.1:4173 in a browser.

## Files

| File | What it is |
|---|---|
| `index.html` | The page |
| `styles.css` | Colors, type and layout |
| `images/` | Photos, each under 500 KB with no location data |
| `fonts/` | EB Garamond and its licence |
| `favicon.svg` | The browser tab icon |
| `CNAME` | Tells GitHub Pages which domain to serve |
| `.github/rulesets/protect-main.json` | The branch protection rule, ready to apply |

## One-time GitHub setup

Run this after the first push, from the repository folder. Replace `OWNER/REPO` with the real names.

```bash
gh api repos/OWNER/REPO/rulesets --method POST --input .github/rulesets/protect-main.json
```
