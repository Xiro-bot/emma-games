---
name: EmmaGames
description: Adopt EmmaGames mode — build, play, and iterate on browser games for Chiro's 5-year-old daughter Emma. Use whenever the conversation is about making a game for Emma, a kids' game, or revisiting games we've built together. On invocation, read GAMES.md (the log of every game) and PLAYBOOK.md (what works for a 5yo) FIRST, then tell Chiro which games already exist before building anything new.
---

# EmmaGames

This is a shared, growing collection of games built for **Emma**, Chiro's daughter. The whole point of this skill is **memory**: so we never start from scratch, and each game gets better as we learn what she likes.

## On every invocation — do this first
1. Read `GAMES.md` (in this skill folder) — the log of every game we've built, where it lives, and its current state.
2. Read `PLAYBOOK.md` — the running list of what works (and doesn't) for a 5-year-old.
3. Briefly tell Chiro: which games already exist, and ask whether he wants to **iterate on an existing one** or **build a new one**.
4. Only then start building.

## After every session — update memory
- If we built or changed a game, update its entry in `GAMES.md` (date, what changed, current state, open feedback items).
- If we learned something about what works for Emma, add a line to `PLAYBOOK.md`.
- Keep both files terse — one game per section, bullet points, newest changes on top.

## About Emma (keep current)
- Age 5. Just lost her **first tooth** (June 2026) — that milestone sparked the first game.
- Plays on a computer with a **mouse**. Games should be mouse-driven, not keyboard.
- Loves: treasure, gold coins, diamonds, hearts, rainbows, fairies, magic wands.
- Needs **Easy by default** — she told us the first version was "too hard." Always ship the gentlest setting first and let difficulty scale up.

## How we build
- **Single self-contained `index.html`** per game (inline CSS + JS, emoji art, no build step, no dependencies). Easy to double-click open and to iterate fast.
- Games live in their own folder under `~/code/emma-games/games/` (e.g. `games/treasure-cups/`). The skill itself lives at `~/code/emma-games/skills/EmmaGames/` and is symlinked into `~/.claude/skills/EmmaGames` (same pattern as the quake skill). The repo is on GitHub — commit + push after a session.
- Big, colorful, friendly visuals. Comic Sans / rounded fonts. Generous animations.
- Always include a clear **reward moment** (fairy, confetti, voice "Congratulations!").
- After building, `open` the file so Chiro can test with Emma, then **iterate on real feedback** — he reviews the first batch with her before we refine.

## Working style with Chiro
- Ship a playable version, then ask 2–4 specific tuning questions (difficulty, speed, length, sound).
- When he reports a bug ("can't see the coin", "looks like stickers"), diagnose the actual cause and fix it — don't just restyle.
