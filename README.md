# Bluebirdle

**Bluebirdle** is a daily Cardiff City FC player guessing game. Work out the mystery Bluebird using clues about their Cardiff City career.

**Play the game:** https://danccfc.github.io/Bluebirdle/

## How to play

- A new mystery player is selected each day.
- Everyone gets the same mystery player for that UTC date.
- You have **five guesses** to find the answer.
- Start typing a player's name and select them from the suggestions.
- After each guess, the clue tiles show how your player compares with the mystery player.

## The clues

Each guess is compared across five categories:

| Clue | What it means |
| --- | --- |
| **Year debuted** | The year the player made their Cardiff City first-team debut. |
| **Nationality** | The player's nationality, displayed with a flag. |
| **Position** | The player's playing position. |
| **Appearances** | Competitive first-team appearances for Cardiff City. |
| **Goals** | Competitive first-team goals for Cardiff City. |

For year debuted, appearances and goals, arrows indicate whether the mystery player's value is higher or lower than your guess. Nationality and position are marked as correct when they match.

Appearances and goals are **Cardiff City totals**, not career totals across all clubs.

## Daily puzzle and stats

- The puzzle resets at **00:00 UTC**.
- Your guesses for the current puzzle are saved in your browser, so they remain after a refresh.
- Played, wins and streak statistics are stored locally in your browser on that device.
- When the game ends, you can share your result.

## Player pool and data

The current pool is the **2026/27 Cardiff City squad**. Earlier seasons are planned for future updates.

Player information is maintained in [`data/players.json`](data/players.json). Each player entry contains:

- `name`
- `debut`
- `nationality`
- `position`
- `appearances`
- `goals`

The appearance and goal figures are Cardiff City competitive first-team totals.

## Hosting

The live game is hosted using GitHub Pages:

https://danccfc.github.io/Bluebirdle/

## Known limitation

The daily answer is selected in the browser from the public `data/players.json` file. Visitors can inspect that file and work out the answer if they want to. Keeping the answer secret would require moving answer selection to a server-side service.

## Disclaimer

Bluebirdle is an independent, unofficial fan-made game. It is not affiliated with, endorsed by, or connected to Cardiff City Football Club.
