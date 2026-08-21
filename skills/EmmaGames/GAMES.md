# Games we built for Emma

_Newest changes on top within each game. One game per section._

> 🌐 **Live website (shareable):** https://xiro-bot.github.io/emma-games/
> GitHub Pages from `Xiro-bot/emma-games` (public), served from `main` root.
> Root `index.html` is the arcade landing page. `git push` → site rebuilds in ~1 min.

---

## 🤡 Clown Balloon Pop
- **Folder:** `~/code/emma-games/games/clown-balloons/index.html` (single file — double-click to play)
- **What it is:** Emma's idea. A big-top circus stage (striped tent roof, red curtains, spotlight cones, gold ring, audience silhouettes bobbing at the bottom). A **CSS-drawn clown** stands centre stage — white face, red nose, blue eyes, orange hair tufts, party hat, ruffle collar, polka-dot suit — and **throws balloons out to the public**, alternating arms (arm swings on each throw).
- **Balloons:** 5 shapes (round, oval, long, ⭐ star, 💗 heart) × 8 colours, all CSS gradients + shine + knot + curly SVG string. They arc out of his hands, then float up with a gentle sway.
- **Mechanics:** the cursor is a **needle** (SVG cursor, hotspot at the tip). Click a balloon → 💥 burst of rubber shreds + "POP!" + WebAudio pop. **Candy is HIDDEN — 1 balloon in 5 holds one and nothing on the outside gives it away**, so it's a hunt: pop as many as you can. A candy pop reveals a golden shockwave ring + "CANDY!" + sparkles, and the candy flies into the **candy jar** HUD (jar fills up, ding sound, counter `n / 10`).
- **Win:** at **10 candies** → clown hops for joy, confetti of 🎈🍬🎉⭐, fanfare, and a spoken "Congratulations Emma! You collected all the candies!" **No timer, no fail state** — popping a plain balloon is just fun, never a penalty.
- **Hit-testing is deliberately forgiving:** the whole bounding box + 18px counts; nearest centre wins when balloons overlap.
- **Difficulty:** 🐢 Easy (default: 124px balloons, slow 26px/s rise, 20% candy, spawn 780ms) / 🤹 Medium (17%) / 🎪 Super Circus (14%, small + fast). ~50 pops per win at 20% — the `candy` dial in `DIFF` is the length knob.
- **Status:** Built 2026-08-21, awaiting Emma's first playtest.

### Open ideas / feedback to revisit
- Candy rate (1 in 5) + rise speed are the two Easy dials most likely to need tuning after she plays.
- Could add a balloon-animal bonus (the long balloons twisting into a dog), or the clown reacting when a balloon is popped.
- Could let the jar be tapped at the end to eat the candies.

### Open ideas / feedback to revisit (cont.)
- Length: 10 candies at 1-in-5 ≈ 50 pops (~2 min of solid popping). If that's too long for her, raise `candy` or drop `GOAL`.

### History
- **2026-08-21** — Chiro's change: **candy is now hidden in any balloon (1 in 5), with no visual tell** — purple became an ordinary colour, the candy-inside/glow/sparkle cues were removed, and the hit-test candy bias was dropped. Added a golden shockwave ring on the reveal so the surprise lands. Easy now spawns faster (780ms, up to 11 on screen) so there's always something to pop.
- **2026-08-21** — First build: circus stage + CSS clown, 5 balloon shapes, needle cursor, purple-candy mechanic (visible candy inside purple balloons), jar HUD, 10-candy win with confetti + voice, 3 difficulties. Added the Clown Balloon Pop card to the arcade landing page.

---

## 🥞 Emma's Crêpe Café
- **Folder:** `~/code/emma-games/games/crepe-cafe/index.html` (single file — double-click to play)
- **What it is:** A crêpe-maker game (Chiro's spec), sequel to Pizza Kitchen with the same cook-bar engine but a full multi-step recipe. Step chips at the top guide the flow: 🥣 Mix → 🌀 Stir → 🔥 Stove → 🍳 Pan → 🫗 Pour → ⏰ Cook & Flip → 🍓 Toppings. A bouncing hint bubble points at whatever to do next.
- **Mechanics:** drag **flour bag / milk carton / egg** (CSS-drawn cards) into the blue bowl (egg shows a cracked yolk). Then **stir by holding the bowl and moving the mouse in circles** — a whisk follows the pointer, batter swirls, progress bar fills (2.5 turns on Easy). Click the **stove knob** (flames ring the burner), drag the **pan** from its hook onto the fire, then drag the **bowl** over the pan — it tilts and pours a batter stream, crêpe spreads in. **Two cook phases** with the zoned cook bar: first DING → click stove to **flip** (jump + squash animation, snapshot of side-1 browning), second DING-DING → click to **plate** (crêpe flies to the plate showing side 1 up). Verdict = worst of both sides: PARFAIT ⭐⭐⭐ / Très bien ⭐⭐ / "a bit crispy — still yummy" ⭐ — **never a fail state**, toppings always follow.
- **Toppings rack** (appears after plating): chocolate drizzle (layer of brown strips), sugar dusting (white dots), strawberries, banana slices, whipped-cream dollops, candy hearts — scatter pieces, tap to remove. Then the **🇫🇷 Bon appétit!** button → confetti + stars + "Congratulations, chef Emma!" voice.
- **Difficulty:** 🐢 Easy (default: 6s window side 1, 5s side 2, 2.5 stir turns) / 🧑‍🍳 Chef / 🔥 Super Chef (more turns, tighter windows). Auto-flips/auto-plates 4s past burnt so it never stalls.
- **Status:** Built 2026-08-08, awaiting Emma's first playtest.

### Open ideas / feedback to revisit
- Stir-in-circles may need tuning for a 5yo mouse grip (turns needed / motion sensitivity).
- Could add butter-in-the-pan step, folding the crêpe, or making a stack of several crêpes.
- Reset is location.reload() — fine for one crêpe at a time; revisit if we add a multi-crêpe stack.

### History
- **2026-08-08** — First build: full mix→stir→stove→pan→pour→flip→plate→toppings flow, two-bell cooking, no-fail verdicts, 6 toppings, bon appétit finale.

---

## 🍕 Emma's Pizza Kitchen
- **Folder:** `~/code/emma-games/games/pizza-kitchen/index.html` (single file — double-click to play)
- **What it is:** A pizza-maker game (Chiro's spec). Left: wooden counter with a dough on a board. Right: **wood-fire brick oven** (animated CSS flames + logs, glowing mouth). Bottom: ingredient rack of 8 CSS-drawn cards — Tomato Sauce, Cheese (layers), Basil, Pepperoni, Mushrooms, Olives, Corn, **Heart Ham** (pink hearts, for Emma). Cursor is an oven mitt 🧤.
- **Mechanics:** drag a card onto the dough → sauce/cheese spread as layers, toppings scatter 5–7 pieces (tap a piece to remove; 🗑️ Start over clears). Drag the whole pizza into the oven → cooking starts. Pizza **browns gradually** (golden overlay → charred overlay). A **cook bar** below the oven shows zones (pale → green ⭐ perfect → burnt) with a moving needle; entering the perfect zone triggers a **WebAudio ding + flashing "⭐ DING! TAKE IT OUT! ⭐" sign + voice**. Click the oven to take it out.
- **Verdicts:** too early → "Still a bit pale!" + **Put it back in!** button (resumes cooking from where it was); perfect → PERFETTO! ⭐⭐⭐ confetti + "Mamma mia!" voice; too late → smoke 💨 + encouraging retry. If never taken out, auto-pulls 4s after fully burnt.
- **Difficulty:** 🐢 Easy (default, 7s perfect window, 26s to burnt) / 🧑‍🍳 Chef / 🔥 Super Chef.
- **Status:** Built 2026-08-08, awaiting Emma's first playtest.

### Open ideas / feedback to revisit
- Could add an "eat it" moment after a perfect pizza (bites disappearing).
- Could let Emma choose pizza size or make pizzas for customers (orders to match).
- Oven-drop hit target: whole oven counts — watch if dragging the pizza there is easy enough for her.

### History
- **2026-08-08** — First build: 8 ingredients, drag-assemble, drag-to-oven, browning + zoned cook bar + ding, three verdicts with put-back-in for undercooked. Also added Fashion Show + Pizza Kitchen cards to the arcade landing page (both were missing).

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
