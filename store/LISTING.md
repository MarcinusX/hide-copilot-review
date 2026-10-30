# Chrome Web Store listing

Copy-paste values for the [Chrome Web Store developer dashboard](https://chrome.google.com/webstore/devconsole).

## Package

Upload `dist/hide-copilot-review-<version>.zip`, built with:

```sh
mkdir -p dist && (cd extension && zip -r ../dist/hide-copilot-review-$(node -p "require('./manifest.json').version").zip .)
```

## Store listing

**Name:** Hide Copilot Review

**Summary:**
Hides the Copilot reviewer suggestion on GitHub pull requests, so you never request a Copilot review by accident.

**Description:**

```
GitHub suggests Copilot as a reviewer on every pull request, with a "Request" button right in the Reviewers sidebar. One misclick and Copilot starts reviewing your PR.

Hide Copilot Review removes it:

• The "Copilot · Balanced · Request" row in the Reviewers sidebar of pull requests
• The same row on the "Open a pull request" page
• The Copilot entry in the reviewers dropdown (your human reviewers stay)

Private and lightweight:
• A single stylesheet injected on github.com
• No JavaScript, no permissions, no tracking, no network requests

Open source (MIT): https://github.com/MarcinusX/hide-copilot-review

Not affiliated with or endorsed by GitHub. "GitHub" and "Copilot" are trademarks of GitHub, Inc.
```

**Category:** Developer Tools
**Language:** English

**Graphic assets:**
- Store icon: `store/icon128.png`
- Screenshot: `store/screenshot-1280x800.png`
- Small promo tile: `store/promo-small-440x280.png`

**Homepage / support URL:** https://github.com/MarcinusX/hide-copilot-review

## Privacy practices

**Single purpose:**
Hides the Copilot reviewer suggestion and its Request button on GitHub pull request pages.

**Host permission justification** (content script on `https://github.com/*`):
The extension injects one CSS file on github.com to hide the Copilot reviewer UI. It does not read page content, run scripts, or send any data.

**Remote code:** No, I am not using remote code.

**Data usage:** Collects none of the listed data types. Tick all three certifications (no selling, no unrelated use, no creditworthiness use).

**Privacy policy URL:** https://github.com/MarcinusX/hide-copilot-review#privacy
