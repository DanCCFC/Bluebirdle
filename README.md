# Bluebirdle

A static, daily Cardiff City player guessing game.

## Run locally
Open `index.html` in a browser, or serve this folder with any static web server.

## Publish online
The easiest option is Netlify:
1. Extract `bluebirdle.zip`.
2. Open Netlify and sign in.
3. Choose **Add new site → Deploy manually**.
4. Drag the extracted `bluebirdle` folder into the deploy area.
5. Netlify will provide a public URL you can share.

It also works on Cloudflare Pages, GitHub Pages and Vercel as a static site.

## Daily puzzle
Everyone gets the same answer on the same UTC date. The puzzle changes at 00:00 UTC. The daily answer is selected deterministically from `data/players.json`.

## Important: player data
This is a functioning first release with a small starter dataset, not yet a complete historical database. Before public launch, expand and verify `data/players.json` so it includes all eligible Cardiff City first-team players from 2012/13 onwards and accurate Cardiff-only competitive totals.

Each player entry uses:
- `name`
- `signed` (first year they joined Cardiff, including loan arrival if that was their first spell)
- `nationality`
- `position` (`Goalkeeper`, `Defender`, `Midfielder`, `Forward`)
- `goals` (Cardiff competitive first-team goals)
- `appearances` (Cardiff competitive first-team appearances)

For managers, do not add entries. This edition is players only.

## Privacy and storage
Game streaks and statistics are stored in the visitor's browser using local storage. No account or server is required. Because this is a static client-side game, its answer data can be inspected by technically curious visitors; a server-backed version would be needed to conceal the daily answer.
