<img src="assets/icon.svg" width="64" height="64" alt="">

# hide-copilot-review

A Chrome extension that hides the **Copilot** reviewer suggestion on GitHub pull requests, so you can't request a Copilot review by accident.

It hides:

- the `Copilot · Balanced ▾ · Request` row in the PR **Reviewers** sidebar
- the same row on the **Open a pull request** (compare) page
- the Copilot entry (and the then-empty "Suggestions" heading) in the reviewers gear dropdown

It's a single CSS file injected on `https://github.com/*`. No JavaScript, no permissions, no network access.

## Install

1. Download this repo (**Code → Download ZIP**, then unzip) or `git clone` it.
2. Open `chrome://extensions`.
3. Turn on **Developer mode** (top right).
4. Click **Load unpacked** and select the `extension/` folder of this repo.

Chrome keeps the extension loaded across restarts. After updating the files, click the reload icon on the extension card.

## Why an extension?

GitHub has no setting to remove Copilot from the reviewer suggestions. Turning off "Copilot code review" in your Copilot settings only stops automatic reviews.

## Notes

- If someone else requests a Copilot review on a PR, Copilot's row in the Reviewers sidebar is hidden too.
- The selectors target GitHub's current markup (the `copilot-pull-request-reviewer` app link and Copilot's user id `175728472`). If GitHub changes the page and Copilot reappears, update `extension/hide-copilot.css`.

## Privacy

The extension collects no data. It only injects a stylesheet on github.com: no JavaScript, no permissions, no network requests.

## License

[MIT](LICENSE). Not affiliated with or endorsed by GitHub. "GitHub" and "Copilot" are trademarks of GitHub, Inc.
