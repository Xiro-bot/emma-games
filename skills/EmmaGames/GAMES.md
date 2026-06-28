# Games we built for Emma

_Newest changes on top within each game. One game per section._

> 🌐 **Live website (shareable):** https://xiro-bot.github.io/emma-games/
> GitHub Pages from `Xiro-bot/emma-games` (public), served from `main` root.
> Root `index.html` is the arcade landing page. `git push` → site rebuilds in ~1 min.

---

## 🏴‍☠️ Pirate Peekaboo
- **Folder:** `~/code/emma-games/games/pirate-barrels/index.html` (single file — double-click to play)
- **What it is:** A pirate reskin of Treasure Cups (Emma's idea). The floor is a **pirate ship deck** (planks + railing + mast/sail with skull + waving 🏴‍☠️ flag, ocean & clouds behind). The cups are **wooden barrels** (staves, metal hoops, ⚓ stamp). Hiding under one barrel is a **glittering treasure pile** — 6 gold coins 🪙 + 9 hand-drawn CSS diamonds in many colors (ruby, orange, yellow, emerald, sky, sapphire, amethyst, pink, teal); coins bob and gems twinkle. Cursor is a **pirate hook 🪝**. Win → the pile pops up huge, confetti of 🏴‍☠️🦜💰⚓💀, and a deep piratey "Arrr! Ye found the treasure, matey!" voice.
- **Same engine** as Treasure Cups: 🐢 Easy / 🦀 Medium / 🦈 Hard, Easy default, slow non-accelerating shuffle.
- **Status:** Built 2026-06-27, awaiting Emma's first playtest.

### History
- **2026-06-27** — Emma's request: replaced the silly hidden pirate with a pile of gold coins + many-colored diamonds (CSS diamonds via clip-path; colors live in the `GEMS` array in the script). Swapped all "pirate"→"treasure" wording + win voice.
- **2026-06-27** — First pirate build (originally had a silly hand-drawn CSS pirate hiding under the barrel).

### Open ideas / feedback to revisit
- Could make the treasure spill/scatter when revealed.
- Could add barrel-roll / wave / coin-jingle sounds.

---

## 🏆 Magic Treasure Cups
- **Folder:** `~/code/emma-games/games/treasure-cups/index.html` (single file — double-click to play)
- **What it is:** A shell/cup game. The treasure (🪙 gold coin + two 💎 diamonds, together in one cup) is shown, then 3 rainbow cups with a 💖 heart shuffle. The mouse pointer is a magic wand 🪄. Pick the right cup → a fairy 🧚 floats in, confetti rains, and it says "Congratulations!" out loud.
- **Status:** Playable. Emma has tested it.

### History
- **2026-06-27** — Added difficulty levels (🐢 Easy / 🐰 Medium / 🚀 Hard), defaulting to Easy, after Emma said it was "too hard." Easy = slow cups that never speed up, 6s shuffle, 3s treasure preview.
- **2026-06-27** — Fixed two bugs from first playtest: (1) coin/diamonds were invisible because the treasure was a child of the cup and lifted with it — moved treasure to sit ON the floor so the cup rises off it; (2) cups "looked like stickers" — rebuilt as rounded 3D domes with cylindrical shading, highlight, hollow rim, and ground shadow.
- **2026-06-27** — First build. 3 cups, 10s shuffle, magic-wand cursor, fairy reward.

### Open ideas / feedback to revisit
- Could add a 2-cup ultra-easy mode for very first wins.
- No background music or click sounds yet — only the spoken "Congratulations!". Could add cheerful sounds.
- Could let the difficulty change the number of cups (e.g. Hard = 4 cups).
