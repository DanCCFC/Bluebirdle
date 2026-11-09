# Bluebirdle

A static, daily Cardiff City player guessing game.

## Run locally

Because the game loads JSON with `fetch()`, serve this folder over HTTP rather than opening `index.html` directly. For example:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Publish with GitHub Pages

1. In this repository, open **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select `main` and `/(root)`, then save.
4. GitHub Pages will publish the site at the URL shown in Settings → Pages.

## Daily puzzle

- Everyone gets the same answer for the same UTC calendar date and the same version of `data/players.json`.
- A new answer is selected at 00:00 UTC.
- Guesses and results persist in the visitor's browser across refreshes for that daily puzzle.
- Streak and record data is stored locally in the visitor's browser.

## Player data schema

Each entry in `data/players.json` must contain:

- `name`
- `signed`: year the player first joined Cardiff (use their first arrival, including a loan, consistently)
- `nationality`
- `position`: `Goalkeeper`, `Defender`, `Midfielder` or `Forward`
- `goals`: competitive first-team goals for Cardiff City
- `appearances`: competitive first-team appearances for Cardiff City

Managers are excluded. Include first-team players who featured from 2012/13 onwards, including loanees.

## Important data status

The current JSON is only a **starter sample**, not a complete or fully verified Cardiff City player database. Do not describe this as a complete historical game until the player list and every statistic have been checked against reliable season-by-season records. In particular, confirm that the signing year and totals are Cardiff-specific and use one consistent competition scope.

## Static-site limitation

The daily answer is selected in the browser from the public JSON file. This means a technically curious visitor can inspect the file and work out the answer for the day. A server-side function/database would be needed to keep the answer secret. For a public hobby game, this static version is simple to host and has no account or server costs.

## Updating the player pool

Edit `data/players.json`. The daily answer schedule is deterministic for a given date and list order; changing or reordering the player list changes the selected answer. Once a public daily schedule starts, avoid changing the list during a live run, or version and announce the reset.
