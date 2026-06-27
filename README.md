# 🎮 Emma Games

Browser games built for Emma (age 5). Each game is a single self-contained
`index.html` — no build step, no dependencies. Just open it in a browser.

## Games

| Game | Folder | What it is |
|------|--------|------------|
| ✨ Magic Treasure Cups | [`games/treasure-cups/`](games/treasure-cups/index.html) | Find the rainbow cup hiding the gold coin + diamonds. Magic-wand cursor, fairy + confetti on a win. |
| 🏴‍☠️ Pirate Peekaboo | [`games/pirate-barrels/`](games/pirate-barrels/index.html) | Pirate-ship reskin: shuffle wooden barrels, hook the one hiding a pile of gold coins & colorful diamonds. |

Both have 🐢 Easy / Medium / Hard difficulty (Easy by default — slow and gentle).

## How to play
Double-click any `index.html`, or:
```sh
open games/treasure-cups/index.html
open games/pirate-barrels/index.html
```
Best on a computer with a mouse (the cursor becomes a wand / hook).

## The EmmaGames skill
[`skills/EmmaGames/`](skills/EmmaGames/) holds the Claude Code skill that
remembers Emma's preferences and the log of every game, so each one builds on
the last. It's symlinked into `~/.claude/skills/EmmaGames` (same pattern as the
quake skill).

- `SKILL.md` — how we build games for Emma
- `GAMES.md` — log of every game + its history
- `PLAYBOOK.md` — what works for a 5-year-old
