# Games we built for Emma

_Newest changes on top within each game. One game per section._

> 🌐 **Live website (shareable):** https://xiro-bot.github.io/emma-games/
> GitHub Pages from `Xiro-bot/emma-games` (public), served from `main` root.
> Root `index.html` is the arcade landing page. `git push` → site rebuilds in ~1 min.

---

## 👗 Emma's Fashion Show
- **Folder:** `~/code/emma-games/games/dressup-show/index.html` (single file — double-click to play)
- **What it is:** A drag-and-drop dress-up game (Emma's idea). A dark stage with red velvet curtains + swag, a pink perspective runway, and **3 girls side by side under spotlight beams** (light cones + feet pools). Each girl starts in a **white sleeveless tee + white underwear**, with 3 different skin/hair combos. Cursor is a magic hand 🤚.
- **Wardrobe rack** (bottom panel, grouped by category, all CSS-drawn — no emoji stickers): 👑 Crowns (gold jeweled crown, pink tiara) · 🌸 Flower headbands (rainbow flower crown, big-flower band) · 🎀 Skirts (rainbow tutu, polka skirt) · 👗 Princess dresses (purple/aqua/rose/sunny ballgowns) · 👠 Fancy shoes (glass slippers, ruby heels, gold flats).
- **Mechanics:** pointer-drag a card up onto a girl → snaps into the right slot (head/body/feet). Slots are single-occupancy so a new dress/skirt swaps the old; new crown swaps old headband. **Tap a worn item to remove it.** `🔄 Undress` clears all. `🌟 Start Show!` (or Enter) = girls curtsy + flash + confetti (🌟💖👑🌈✨) + spoken "Wow! You look so beautiful!". Slot z-order: head 40 / feet 26 / body 20 over the base model.
- **Status:** Built 2026-07-01, awaiting Emma's first playtest.

### Open ideas / feedback to revisit
- Could add hair styling (bows/ribbons), necklaces/wings, or a wand accessory.
- Could add a "camera flash / photo" moment per girl, or let Emma pick backdrop colors.
- Drag onto the closest girl works via elementFromPoint — watch that dropping precisely on a girl is easy enough for her; may need bigger hit targets.

### History
- **2026-07-01** — Emma's request: added two **cat-print dresses** (pink + blue) — a CSS-drawn white kitty face (pink ears, shiny eyes, nose, whiskers) on the skirt, via a new `deco` param on `dress()` + `catFace()` helper. Plain dresses still available. Open follow-ups Emma may want: cat on skirts, other cat colors, or more animal prints (bunny/unicorn/puppy).
- **2026-07-01** — First build: spotlight fashion-show scene, 3 base models, 5 wardrobe categories, pointer drag-drop, tap-to-remove, curtsy+confetti+voice reward.

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
